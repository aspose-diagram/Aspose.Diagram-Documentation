---
title: Bearbeiten Sie die eingebetteten OLE-Objekte in Visio Diagram
type: docs
weight: 10
url: /de/net/manipulate-the-embedded-ole-objects-in-visio-diagram/
description: Diese Seite beschreibt, wie man ein Ole-Objekt mit der Bibliothek Aspose.Diagram manipuliert.
---
{{% alert color="primary" %}}

Microsoft Office Visio unterstützt die Bearbeitung der OLE-Objekte in Visio diagram. Wenn sich eine visio-Datei außerhalb der Visio-Zeichnung befindet und Entwickler eine Funktion in ihren .NET-Anwendungen hinzufügen müssen, um diese Dateien automatisch in die Zeichnung einzufügen, können sie dies erreichen, indem sie verwenden[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

{{% /alert %}}
## **Bearbeiten Sie das Programmierbeispiel für eingebettete OLE-Objekte**
[Objektdaten](http://www.aspose.com/api/net/diagram/aspose.diagram/foreigndata/properties/objectdata) Eigentum der[Ausländische Daten](http://www.aspose.com/api/net/diagram/aspose.diagram/foreigndata)Klasse ermöglicht es Entwicklern, vorhandene OLE-Objekte in Visio diagram zu manipulieren. Dieses Hilfethema zeigt, wie Entwickler ein OLE-Objekt des Word-Dokuments abrufen und bearbeiten können[Aspose.Words for .NET API](https://products.aspose.com/words/net), und speichern Sie sie dann als OLE-Objekt in Visio diagram zurück.


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

