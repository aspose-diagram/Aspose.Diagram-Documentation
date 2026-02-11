---
title: Travailler avec l'impression
type: docs
weight: 80
url: /fr/net/working-with-print/
description: This section explains how to print a document via XpsPrint with Aspose.Diagram.
---
## **How to Print a Document on a Server via the XpsPrint API**
This article can be useful to anyone who wants to submit an XPS document to the unmanaged XpsPrint API from a .NET application. But the main goal if this article is to show how to print a diagram from an ASP.NET or Windows Service application using Aspose.Diagram and the XpsPrint API.
### **Problème**
Lorsque vous développez une application .NET et que vous devez produire une sortie imprimée, vous pouvez utiliser les classes de l'espace de noms System.Drawing.Printing ou les classes WPF. Mais, il s'avère que si vous développez une application de service ASP.NET ou Windows, vos options d'impression sont fortement limitées, car Microsoft déconseille l'utilisation de ces approches. Voir les liens ci-dessous pour plus d'informations.

<http://support.microsoft.com/kb/324565>

L'utilisation des classes d'impression .NET Framework n'est pas prise en charge à partir d'un service. Cela inclut les pages ASP, qui s'exécutent généralement dans le contexte du service serveur.

<http://msdn.microsoft.com/en-us/library/system.drawing.printing.aspx>

Les classes au sein de l'espace de noms System.Drawing.Printing ne sont pas prises en charge pour une utilisation dans un service Windows ou une application ou un service ASP.NET. Tenter d'utiliser ces classes à partir de l'un de ces types d'application peut entraîner des problèmes inattendus, tels que des performances de service réduites et des exceptions d'exécution.

<http://msdn.microsoft.com/en-us/library/bb613549.aspx>

L'utilisation de WPF pour créer les services Windows n'est pas prise en charge. Étant donné que WPF est une technologie de présentation, le service Windows nécessite les autorisations appropriées pour effectuer des opérations visuelles impliquant une interaction de l'utilisateur. Si le service Windows ne dispose pas des autorisations appropriées, des résultats inattendus peuvent se produire.

The Document object provides a family of the Print methods to print documents and these methods print via the .NET printing classes defined in the System.Drawing.Printing namespace. There are many customers of Aspose.Diagram who use this printing method in their server-side applications without any problems, but there is a way to comply with Microsoft’s recommendations and it is described in this article.
### **La solution**
La bonne façon d'imprimer des documents selon Microsoft est d'utiliser XpsPrint API non géré. Ce API est disponible sur Windows 7, Windows Server 2008 R2 et également sur Windows Vista, à condition que la mise à jour de la plate-forme pour Windows Vista soit installée.

Since Aspose.Diagram can easily convert any document to XPS, we only need to write code that passes an XPS document to the XpsPrint API. The only problem is that the XpsPrint API is unmanaged and it requires some knowledge of the Platform Invoke.
### **Le code**
Nous avons créé la classe XpsPrintHelper avec la méthode Print, qui est très facile à utiliser. Il vous suffit de spécifier un document que vous souhaitez imprimer, un nom d'imprimante et un nom de travail facultatif. En cas de problème lors de la soumission ou de l'impression du document, la méthode lèvera une exception.

Le dernier paramètre est une valeur booléenne qui spécifie si le code doit attendre que le travail soit imprimé ou revenir immédiatement après que le travail d'impression a été soumis. Si vous choisissez de revenir immédiatement, vous ne pourrez pas déterminer si le document s'est imprimé avec succès ou non à la fin.
#### **Exemple de programmation**
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
#### **Exemple de programmation XpsPrint API**
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



Le code des méthodes StartJob, CopyJob, WaitForJob et CheckJobStatus ainsi que les définitions des interfaces IXpsPrintJob et IXpsPrintJobStream est assez bas niveau et utilise Platform Invoke et COM Interop. Ce code n'est pas inclus dans l'article par souci de concision, mais il est disponible dans l'exemple de téléchargement.

Le XpsPrint API fournit également des fonctionnalités supplémentaires, telles que la surveillance de la progression du travail, mais notre XpsPrintHelper est un wrapper très simple et n'expose pas cette fonctionnalité. Vous pouvez l'ajouter vous-même si vous le souhaitez.

{{% alert color="primary" %}}

Lorsque vous exécutez le projet, il imprime un exemple de document sur l'imprimante spécifiée. Pour rendre les résultats visibles, la fenêtre de la console s'ouvre. Le programme affiche le message de réussite ou le texte d'une exception si une a été levée.

{{% /alert %}}
## **Impression d'un Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) fournit quatre méthodes de surcharge pour l'impression des diagrammes. Ces méthodes sont suffisamment flexibles pour imprimer le diagram sur l'imprimante par défaut ou sur l'une des imprimantes disponibles avec des paramètres personnalisés. Il vous suffit de sélectionner la méthode d'impression appropriée en fonction des besoins.
### **Impression sur l'imprimante par défaut**
L'impression du diagram sur l'imprimante par défaut est assez simple dans Aspose.Diagram for .NET. Effectuez les étapes suivantes pour imprimer le diagram sur l'imprimante par défaut :

- Créez une instance de la classe Diagram pour charger un diagram à imprimer
- Appelez la méthode Print sans paramètres comme exposé par l'objet Diagram
#### **Impression sur un exemple de programmation d'imprimante par défaut**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Call the print method to print whole Diagram using the default printer
diagram.Print();

{{< /highlight >}}

### **Impression sur une imprimante spécifique**
L'impression du diagram sur l'imprimante spécifique nécessite le nom de l'imprimante comme paramètre de la méthode d'impression du Diagram. Effectuez les étapes suivantes afin d'imprimer le diagram sur l'imprimante souhaitée :

- Créez une instance de la classe Diagram pour charger un diagram à imprimer
- Appelez la méthode Print de la classe Diagram avec le nom de l'imprimante comme paramètre de chaîne à la méthode Print
#### **Impression sur un exemple de programmation d'imprimante spécifique**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Call the print method to print whole Diagram using the printer name
diagram.Print("LaserJet1100");

{{< /highlight >}}

### **Définition de l'imprimante et du nom du document**
Aspose.Diagram Les API permettent de définir l'imprimante spécifique et le nom du document pour un travail d'impression. Effectuez les étapes suivantes afin d'imprimer le diagram sur l'imprimante souhaitée :

- Créez une instance de la classe Diagram pour charger un diagram à imprimer
- Appelez la méthode Print de la classe Diagram avec l'imprimante et le nom du document comme paramètre de chaîne à la méthode Print
#### **Configuration de l'imprimante et du nom du document Exemple de programmation**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Call the print method to print whole Diagram using the printer name and set document name in the print job
diagram.Print("LaserJet1100", "Job name while printing with Aspose.Diagram");

{{< /highlight >}}

