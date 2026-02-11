---
title: Manipolare gli oggetti OLE incorporati in Visio Diagram
type: docs
weight: 10
url: /it/net/manipulate-the-embedded-ole-objects-in-visio-diagram/
description: Questa pagina descrive come manipolare un oggetto ole con la libreria Aspose.Diagram.
---
{{% alert color="primary" %}}

Microsoft Office Visio supporta la manipolazione degli oggetti OLE nel disegno Visio diagram.[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

{{% /alert %}}
## **Manipolare l'esempio di programmazione di oggetti OLE incorporati**
[ObjectData](http://www.aspose.com/api/net/diagram/aspose.diagram/foreigndata/properties/objectdata) proprietà del[Dati Esteri](http://www.aspose.com/api/net/diagram/aspose.diagram/foreigndata)consente agli sviluppatori di manipolare oggetti OLE esistenti in Visio diagram. Questo argomento della guida mostra come gli sviluppatori possono recuperare un oggetto OLE del documento Word, modificarlo utilizzando[Aspose.Words for .NET API](https://products.aspose.com/words/net), quindi salvare di nuovo come oggetto OLE in Visio diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_OLEObjects();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page of the Visio diagram by name
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");
// Get shape of the Visio diagram by ID
Aspose.Diagram.Shape OLE_Shape = page.Shapes.GetShape(2);

// Filter shapes by type Foreign
if (OLE_Shape.Type == Aspose.Diagram.TypeValue.Foreign)
{
    if (OLE_Shape.ForeignData.ForeignType == ForeignType.Object)
    {
        Stream Ole_stream = new MemoryStream(OLE_Shape.ForeignData.ObjectData);
        // Get format of the OLE file object
        Aspose.Words.FileFormatInfo info = Aspose.Words.FileFormatUtil.DetectFileFormat(Ole_stream);
        if (info.LoadFormat == Aspose.Words.LoadFormat.Doc || info.LoadFormat == Aspose.Words.LoadFormat.Docx)
        {
            // Modify an OLE object
            var doc = new Aspose.Words.Document(new MemoryStream(OLE_Shape.ForeignData.ObjectData));
            doc.Range.Replace("testing", "Aspose", false, true);
            MemoryStream outStream = new MemoryStream();
            doc.Save(outStream, Aspose.Words.SaveFormat.Docx);
            // Save back an OLE object
            OLE_Shape.ForeignData.ObjectData = outStream.ToArray();
        }
    }
}
// Save Visio diagram
diagram.Save(dataDir + "ManipulateObjects_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

