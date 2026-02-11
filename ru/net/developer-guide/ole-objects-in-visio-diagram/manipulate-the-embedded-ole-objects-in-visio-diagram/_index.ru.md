---
title: Управление встроенными объектами OLE в Visio Diagram
type: docs
weight: 10
url: /ru/net/manipulate-the-embedded-ole-objects-in-visio-diagram/
description: На этой странице описывается, как управлять объектами ole с библиотекой Aspose.Diagram.
---
{{% alert color="primary" %}}

Microsoft Office Visio поддерживает управление объектами OLE в Visio diagram. Если файл visio находится за пределами чертежа Visio и разработчикам необходимо добавить в свои приложения .NET функцию для автоматической вставки этих файлов внутрь чертежа, они могут добиться этого с помощью[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

{{% /alert %}}
## **Управление примером программирования встроенных объектов OLE**
[ObjectData](http://www.aspose.com/api/net/diagram/aspose.diagram/foreigndata/properties/objectdata) собственность[Иностранные данные](http://www.aspose.com/api/net/diagram/aspose.diagram/foreigndata)Класс позволяет разработчикам манипулировать существующими объектами OLE в Visio diagram. В этом разделе справки показано, как разработчики могут получить объект OLE документа Word, отредактировать его с помощью[Aspose.Words for .NET API](https://products.aspose.com/words/net), а затем сохраните обратно как объект OLE в файле Visio diagram.


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

