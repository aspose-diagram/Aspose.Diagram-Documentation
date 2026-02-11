---
title: Manipulate the Embedded OLE Objects in Visio Diagram
type: docs
weight: 10
url: /net/manipulate-the-embedded-ole-objects-in-visio-diagram/
description: This page describes how to manipulate ole object with Aspose.Diagram library.
---

{{% alert color="primary" %}}

Microsoft Office Visio supports manipulating the OLE objects in the Visio diagram. If an visio file resides outside of the Visio drawing and developers need to add a feature in their .NET applications to auto insert these files inside of the drawing, they can achieve this by using [Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

{{% /alert %}}
## **Manipulate the Embedded OLE Objects Programming Sample**
[ObjectData](http://www.aspose.com/api/net/diagram/aspose.diagram/foreigndata/properties/objectdata) property of the [ForeignData](http://www.aspose.com/api/net/diagram/aspose.diagram/foreigndata) class allows developers to manipulate with existing OLE objects in Visio diagram. This help topic demonstrates how developers can retrieve an OLE object of the Word document, edit it using [Aspose.Words for .NET API](https://products.aspose.com/words/net), and then save back as an OLE object in the Visio diagram.


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

