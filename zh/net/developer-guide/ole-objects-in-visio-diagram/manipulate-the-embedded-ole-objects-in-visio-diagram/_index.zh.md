---
title: 操作 Visio 中的嵌入式 OLE 对象 Diagram
type: docs
weight: 10
url: /zh/net/manipulate-the-embedded-ole-objects-in-visio-diagram/
description: 本页介绍如何使用 Aspose.Diagram 库操作 ole 对象。
---
{{% alert color="primary" %}}

Microsoft Office Visio 支持操作 Visio diagram 中的 OLE 对象。如果 visio 文件位于 Visio 绘图之外，开发人员需要在其 .NET 应用程序中添加一项功能以自动将这些文件插入绘图内部，他们可以通过使用[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

{{% /alert %}}
## **操作嵌入式 OLE 对象编程示例**
[对象数据](http://www.aspose.com/api/net/diagram/aspose.diagram/foreigndata/properties/objectdata)的财产[外国数据](http://www.aspose.com/api/net/diagram/aspose.diagram/foreigndata)类允许开发人员操作 Visio diagram 中的现有 OLE 对象。此帮助主题演示开发人员如何检索 Word 文档的 OLE 对象，使用[Aspose.Words for .NET API](https://products.aspose.com/words/net)然后在 Visio diagram 中存回一个 OLE 对象。


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

