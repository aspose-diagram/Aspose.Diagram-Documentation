---
title: 操作 Visio 中的嵌入式 OLE 对象 Diagram
type: docs
weight: 10
url: /zh/java/manipulate-the-embedded-ole-objects-in-visio-diagram/
description: 本页介绍如何使用 Aspose.Diagram 库操作 ole 对象。
---
{{% alert color="primary" %}}

Microsoft Office Visio 支持操作 Visio diagram 中的 OLE 对象。如果 visio 文件位于 Visio 绘图之外，开发人员需要在其 Java 应用程序中添加一项功能以自动将这些文件插入绘图内部，他们可以通过使用[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

{{% /alert %}}
## **操作嵌入式 OLE 对象编程示例**
[对象数据](https://reference.aspose.com/diagram/java/com.aspose.diagram/foreigndata#ObjectData)的财产[外国数据](https://reference.aspose.com/diagram/java/com.aspose.diagram/foreigndata)类允许开发人员操作 Visio diagram 中的现有 OLE 对象。此帮助主题演示开发人员如何检索 Visio 文档的 OLE 对象，使用[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java)然后在 Visio diagram 中存回一个 OLE 对象。

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
String dataDir = Utils.getDataDir(ManipulateEmbeddedOLEObjects.class);
System.out.println(dataDir);
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page of the Visio diagram by name
Page page = diagram.getPages().getPage("Page-1");
// get shape of the Visio diagram by ID
Shape OLE_Shape = page.getShapes().getShape(2);

// filter shapes by type Foreign
if (OLE_Shape.getType() == TypeValue.FOREIGN) {
	if (OLE_Shape.getForeignData().getForeignType() == ForeignType.OBJECT) {
		ByteArrayInputStream Ole_stream = new ByteArrayInputStream(OLE_Shape.getForeignData().getObjectData());
		// get format of the OLE file object
		com.aspose.words.FileFormatInfo info = com.aspose.words.FileFormatUtil.detectFileFormat(Ole_stream);
		if (info.getLoadFormat() == com.aspose.words.LoadFormat.DOC
				|| info.getLoadFormat() == com.aspose.words.LoadFormat.DOCX) {
			// modify an OLE object using Aspose.Words API
			Document doc = new Document(new ByteArrayInputStream(OLE_Shape.getForeignData().getObjectData()));
			doc.getRange().replace("testing", "Aspose", false, true);
			ByteArrayOutputStream outStream = new ByteArrayOutputStream();
			doc.save(outStream, com.aspose.words.SaveFormat.DOCX);
			// replace an OLE object
			OLE_Shape.getForeignData().setObjectData(outStream.toByteArray());
		}
	}
}
// save Visio diagram
diagram.save(dataDir + "modified.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
