---
title: Pubblico API Modifiche Aspose.Diagram 6.6.0
type: docs
weight: 20
url: /it/net/public-api-changes-in-aspose-diagram-6-6-0/
---
{{% alert color="primary" %}} 

Questo documento descrive le modifiche allo Aspose.Diagram API dalla versione 6.3.0 alla 6.6.0, che potrebbero interessare gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte in Aspose.Diagram.

{{% /alert %}} 
## **Aggiunge i formati VSDM, VSSM e VSTM nella classe LoadFileFormat**
Questa versione aggiunge il supporto per la lettura dei formati Visio abilitati per le macro.
## **Aggiunge i formati VSDM, VSSM e VSTM nella classe SaveFileFormat**
Questa versione aggiunge il supporto per la scrittura di formati Visio abilitati per le macro.
## **Modifica il codice del modulo VBA nel Visio Diagram**
Abbiamo aggiunto le classi VbaModule, VbaModuleCollection, VbaProject, VbaProjectReference e VbaProjectReferenceCollection. Queste classi aiutano a ottenere il controllo sul progetto VBA. Utilizzando questa nuova versione 6.6.0 o successiva, gli sviluppatori possono estrarre e modificare il codice del modulo VBA. Si prega di controllare questo esempio di codice:

**C#**

{{< highlight "csharp" >}}

 // load an existing Visio diagram

Diagram diagram = new Diagram(@"c:\temp\macro.vsdm", LoadFileFormat.VSDM);

// extract VBA project

Aspose.Diagram.Vba.VbaProject v = diagram.VbaProject;

// Iterate through the modules and modify VBA module code

foreach (VbaModule module in diagram.VbaProject.Modules)

{

    string code = module.Codes;

    if (code.Contains("This is test message."))

        code = code.Replace("This is test message.", "This is Aspose.Diagram message.");

    module.Codes = code;

}

// save the Visio diagram

diagram.Save(@"c:\temp\out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}

Errore durante il rendering della macro 'codice': valore non valido specificato per il parametro lang
## **Aggiunge una proprietà ImageData nella classe ForeignData**
Rappresenta un'immagine di un oggetto ole come un array di byte. Oltre a questo, abbiamo anche migliorato la manipolazione degli oggetti OLE. Gli sviluppatori ora possono anche sostituire un oggetto OLE nel Visio diagram. Controlla questo esempio di codice:

**C#**

{{< highlight "csharp" >}}

 // load a Visio diagram

Diagram diagram = new Diagram(DirPath + "Drawing1.vsdx");

// get page of the Visio diagram by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// get shape of the Visio diagram by ID

Aspose.Diagram.Shape OLE_Shape = page.Shapes.GetShape(2);

// filter shapes by type Foreign

if (OLE_Shape.Type == Aspose.Diagram.TypeValue.Foreign)

{

    if (OLE_Shape.ForeignData.ForeignType == ForeignType.Object)

    {

        Stream Ole_stream = new MemoryStream(OLE_Shape.ForeignData.ObjectData);

        // get format of the OLE file object

        Aspose.Words.FileFormatInfo info = Aspose.Words.FileFormatUtil.DetectFileFormat(Ole_stream);

        if (info.LoadFormat == Aspose.Words.LoadFormat.Doc || info.LoadFormat == Aspose.Words.LoadFormat.Docx)

        {

            // modify an OLE object

            var doc = new Aspose.Words.Document(new MemoryStream(OLE_Shape.ForeignData.ObjectData));

            doc.Range.Replace("testing", "Aspose", false, true);

            MemoryStream outStream = new MemoryStream();

            doc.Save(outStream, Aspose.Words.SaveFormat.Docx);

            // save back an OLE object

            OLE_Shape.ForeignData.ObjectData = outStream.ToArray();

        }

    }

}

// save Visio diagram

diagram.Save(DirPath + "modified.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Errore durante il rendering della macro 'codice': valore non valido specificato per il parametro lang
