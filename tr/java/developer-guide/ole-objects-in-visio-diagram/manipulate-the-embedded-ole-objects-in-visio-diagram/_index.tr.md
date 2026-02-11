---
title: Visio Diagram'de Katıştırılmış OLE Nesnelerini Yönetin
type: docs
weight: 10
url: /tr/java/manipulate-the-embedded-ole-objects-in-visio-diagram/
description: Bu sayfa, ole nesnesinin Aspose.Diagram kitaplığıyla nasıl değiştirileceğini açıklar.
---
{{% alert color="primary" %}}

Microsoft Office Visio, Visio diagram içindeki OLE nesnelerinin değiştirilmesini destekler. Bir visio dosyası Visio çiziminin dışında bulunuyorsa ve geliştiricilerin bu dosyaları çizimin içine otomatik olarak eklemek için Java uygulamalarına bir özellik eklemeleri gerekiyorsa, bunu kullanarak başarabilirler.[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

{{% /alert %}}
## **Gömülü OLE Nesneleri Programlama Örneğinin İşlenmesi**
[Nesne Verileri](https://reference.aspose.com/diagram/java/com.aspose.diagram/foreigndata#ObjectData) mülkiyeti[Yabancı Veri](https://reference.aspose.com/diagram/java/com.aspose.diagram/foreigndata) sınıfı, geliştiricilerin Visio diagram'deki mevcut OLE nesnelerini işlemesine olanak tanır. Bu yardım konusu, geliştiricilerin Visio belgesinin bir OLE nesnesini nasıl alıp, kullanarak düzenleyebileceğini gösterir.[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java)ve ardından Visio diagram'de bir OLE nesnesi olarak geri kaydedin.

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
