---
title: Lavorare con Stampa
type: docs
weight: 80
url: /it/net/working-with-print/
description: This section explains how to print a document via XpsPrint with Aspose.Diagram.
---
## **How to Print a Document on a Server via the XpsPrint API**
This article can be useful to anyone who wants to submit an XPS document to the unmanaged XpsPrint API from a .NET application. But the main goal if this article is to show how to print a diagram from an ASP.NET or Windows Service application using Aspose.Diagram and the XpsPrint API.
### **Problema**
Quando sviluppi un'applicazione .NET e devi produrre un output stampato, puoi usare le classi nello spazio dei nomi System.Drawing.Printing o le classi WPF. Ma, a quanto pare, se sviluppi un'applicazione di servizio ASP.NET o Windows, le tue opzioni per la stampa sono fortemente limitate, perché Microsoft consiglia di non utilizzare questi approcci. Vedere i collegamenti sottostanti per ulteriori informazioni.

<http://support.microsoft.com/kb/324565>

L'utilizzo delle classi di stampa .NET Framework non è supportato da un servizio. Ciò include le pagine ASP, che generalmente vengono eseguite nel contesto del servizio server.

<http://msdn.microsoft.com/en-us/library/system.drawing.printing.aspx>

Le classi all'interno dello spazio dei nomi System.Drawing.Printing non sono supportate per l'uso all'interno di un servizio Windows o di un'applicazione o servizio ASP.NET. Il tentativo di utilizzare queste classi dall'interno di uno di questi tipi di applicazione può produrre problemi imprevisti, come prestazioni del servizio ridotte ed eccezioni di runtime.

<http://msdn.microsoft.com/en-us/library/bb613549.aspx>

L'uso di WPF per creare i servizi Windows non è supportato. Poiché WPF è una tecnologia di presentazione, il servizio Windows richiede le autorizzazioni appropriate per eseguire operazioni visive che implicano l'interazione dell'utente. Se il servizio Windows non dispone delle autorizzazioni appropriate, potrebbero verificarsi risultati imprevisti.

The Document object provides a family of the Print methods to print documents and these methods print via the .NET printing classes defined in the System.Drawing.Printing namespace. There are many customers of Aspose.Diagram who use this printing method in their server-side applications without any problems, but there is a way to comply with Microsoft’s recommendations and it is described in this article.
### **Soluzione**
Il modo corretto per stampare documenti secondo Microsoft è utilizzare XpsPrint API non gestito. Questo API è disponibile su Windows 7, Windows Server 2008 R2 e anche su Windows Vista, a condizione che sia installato l'aggiornamento della piattaforma per Windows Vista.

Since Aspose.Diagram can easily convert any document to XPS, we only need to write code that passes an XPS document to the XpsPrint API. The only problem is that the XpsPrint API is unmanaged and it requires some knowledge of the Platform Invoke.
### **Il codice**
Abbiamo creato la classe XpsPrintHelper con il metodo Print, che è molto facile da usare. Devi solo specificare un documento che desideri stampare, un nome stampante e un nome lavoro facoltativo. In caso di problemi durante l'invio o la stampa del documento, il metodo genererà un'eccezione.

L'ultimo parametro è un valore booleano che specifica se il codice deve attendere finché il lavoro non viene stampato o tornare immediatamente dopo l'invio del lavoro di stampa. Se scegli di restituire immediatamente, non sarai in grado di determinare se il documento è stato stampato correttamente o meno alla fine.
#### **Esempio di programmazione**
The following code example shows how to invoke the utility class to print via XPS.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
// Specify the name of the printer you want to print to.
const string printerName = @"\\COMPANY\Brother MFC-885CW Printer";

// Print the document.
XpsPrintHelper.Print(diagram, printerName, "My Test Job", true);

{{< /highlight >}}



There are two overloads of the XpsPrintHelper.Print method. The first overload takes an Aspose.Diagram.Diagram object and saves it into a MemoryStream in the XPS format. Then it invokes the other XpsPrintHelper.Print overload.

If you want to use this sample without Aspose.Diagram (e.g. you already have an XPS document and just want to print it from an ASP.NET or Windows Service application), then you can just delete this method.
#### **XPS Stream and Print Programming Sample**
This code example convert a Diagram into an XPS stream and print.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
/// <summary>
/// Sends an Aspose.Diagram document to a printer using the XpsPrint API.
/// </summary>
/// <param name="diagram"></param>
/// <param name="printerName"></param>
/// <param name="jobName">Job name. Can be null.</param>
/// <param name="isWait">True to wait for the job to complete. False to return immediately after submitting the job.</param>
/// <exception cref="Exception">Thrown if any error occurs.</exception>
public static void Print(Diagram diagram, string printerName, string jobName, bool isWait)
{
    if (diagram == null)
        throw new ArgumentNullException("document");

    // Use Aspose.Diagram to convert the document to XPS and store in a memory stream.
    MemoryStream stream = new MemoryStream();
    diagram.Save(stream, SaveFileFormat.XPS);
    stream.Position = 0;

    Print(stream, printerName, jobName, isWait);
}

{{< /highlight >}}



The second XpsPrintHelper.Print overload accepts a Stream object. The stream must contain a document in the XPS format. This method starts an XPS print job, sends the document to the XpsPrint API and then waits for the result if needed.
#### **Esempio di programmazione XpsPrint API**
This code example prints an XPS document using the XpsPrint API.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
/// <summary>
/// Sends a stream that contains a document in the XPS format to a printer using the XpsPrint API.
/// Has no dependency on Aspose.Diagram, can be used in any project.
/// </summary>
/// <param name="stream"></param>
/// <param name="printerName"></param>
/// <param name="jobName">Job name. Can be null.</param>
/// <param name="isWait">True to wait for the job to complete. False to return immediately after submitting the job.</param>
/// <exception cref="Exception">Thrown if any error occurs.</exception>
public static void Print(Stream stream, string printerName, string jobName, bool isWait)
{
    if (stream == null)
        throw new ArgumentNullException("stream");
    if (printerName == null)
        throw new ArgumentNullException("printerName");

    // Create an event that we will wait on until the job is complete.
    IntPtr completionEvent = CreateEvent(IntPtr.Zero, true, false, null);
    if (completionEvent == IntPtr.Zero)
        throw new Win32Exception();

    try
    {
        IXpsPrintJob job;
        IXpsPrintJobStream jobStream;
        StartJob(printerName, jobName, completionEvent, out job, out jobStream);

        CopyJob(stream, job, jobStream);

        if (isWait)
        {
            WaitForJob(completionEvent);
            CheckJobStatus(job);
        }
    }
    finally
    {
        if (completionEvent != IntPtr.Zero)
            CloseHandle(completionEvent);
    }
}

{{< /highlight >}}



Il codice per i metodi StartJob, CopyJob, WaitForJob e CheckJobStatus, nonché le definizioni delle interfacce IXpsPrintJob e IXpsPrintJobStream, è di basso livello e utilizza Platform Invoke e COM Interop. Questo codice non è incluso nell'articolo per brevità, ma è disponibile nel download di esempio.

XpsPrint API fornisce anche funzionalità aggiuntive, come il monitoraggio dell'avanzamento del lavoro, ma il nostro XpsPrintHelper è un wrapper molto semplice e non espone questa funzionalità. Puoi aggiungerlo tu stesso se vuoi.

{{% alert color="primary" %}}

Quando si esegue il progetto, viene stampato un documento di esempio sulla stampante specificata. Per rendere visibili i risultati, si apre la finestra della console. Il programma visualizza il messaggio di successo o il testo di un'eccezione se ne è stata generata una.

{{% /alert %}}
## **Stampa un Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) fornisce quattro metodi di overload per la stampa dei diagrammi. Questi metodi sono sufficientemente flessibili per stampare lo diagram sulla stampante predefinita o su qualsiasi stampante disponibile con impostazioni personalizzate. Devi solo selezionare il metodo di stampa appropriato in base al requisito.
### **Stampa sulla stampante predefinita**
La stampa di diagram sulla stampante predefinita è abbastanza semplice in Aspose.Diagram for .NET. Effettuare le seguenti operazioni per stampare diagram sulla stampante predefinita:

- Crea un'istanza della classe Diagram per caricare un diagram che deve essere stampato
- Chiamare il metodo Print senza parametri come esposto dall'oggetto Diagram
#### **Esempio di programmazione della stampa su stampante predefinita**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Call the print method to print whole Diagram using the default printer
diagram.Print();

{{< /highlight >}}

### **Stampa su stampante specifica**
La stampa dello diagram sulla stampante specifica richiede il nome della stampante come parametro per il metodo di stampa dello Diagram. Effettuare le seguenti operazioni per stampare lo diagram sulla stampante desiderata:

- Crea un'istanza della classe Diagram per caricare un diagram che deve essere stampato
- Chiamare il metodo Print della classe Diagram con il nome della stampante come parametro di stringa al metodo Print
#### **Esempio di programmazione della stampa su una stampante specifica**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Call the print method to print whole Diagram using the printer name
diagram.Print("LaserJet1100");

{{< /highlight >}}

### **Impostazione della stampante e del nome del documento**
Aspose.Diagram API consente di impostare la stampante specifica e il nome del documento per un lavoro di stampa. Effettuare le seguenti operazioni per stampare lo diagram sulla stampante desiderata:

- Crea un'istanza della classe Diagram per caricare un diagram che deve essere stampato
- Chiamare il metodo Print della classe Diagram con la stampante e il nome del documento come parametro di stringa al metodo Print
#### **Impostazione della stampante e del nome del documento Esempio di programmazione**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Call the print method to print whole Diagram using the printer name and set document name in the print job
diagram.Print("LaserJet1100", "Job name while printing with Aspose.Diagram");

{{< /highlight >}}

