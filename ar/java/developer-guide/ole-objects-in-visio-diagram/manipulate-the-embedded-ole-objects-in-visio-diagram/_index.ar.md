---
title: معالجة كائنات OLE المضمنة في Visio Diagram
type: docs
weight: 10
url: /ar/java/manipulate-the-embedded-ole-objects-in-visio-diagram/
description: توضح هذه الصفحة كيفية التعامل مع كائن Oole باستخدام مكتبة Aspose.Diagram.
---
{{% alert color="primary" %}}

Microsoft Office Visio يدعم معالجة كائنات OLE في Visio diagram. إذا كان ملف visio موجودًا خارج الرسم Visio ويحتاج المطورون إلى إضافة ميزة في تطبيقاتهم Java لإدراج هذه الملفات تلقائيًا داخل الرسم ، فيمكنهم تحقيق ذلك باستخدام[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

{{% /alert %}}
## **معالجة نموذج برمجة كائنات OLE المضمنة**
[بيانات الكائن](https://reference.aspose.com/diagram/java/com.aspose.diagram/foreigndata#ObjectData) ممتلكات[ForeignData](https://reference.aspose.com/diagram/java/com.aspose.diagram/foreigndata) تسمح الفئة للمطورين بالتعامل مع كائنات OLE الموجودة في Visio diagram. يوضح موضوع التعليمات هذا كيف يمكن للمطورين استرداد كائن OLE من مستند Visio ، وتحريره باستخدام[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java)، ثم قم بالحفظ مرة أخرى ككائن OLE في Visio diagram.


{{< highlight java >}}
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

