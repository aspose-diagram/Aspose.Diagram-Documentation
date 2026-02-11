---
title: احصل على عرض الورق وارتفاع الصفحة
type: docs
weight: 50
url: /ar/java/get-paper-width-and-height-of-page/
description: يوضح هذا القسم كيفية الحصول على حجم ورق لصفحة visio مع Aspose.Diagram.
---
## **سيناريوهات الاستخدام الممكنة**

في بعض الأحيان ، تحتاج إلى معرفة عرض وارتفاع حجم الورق حيث تم ضبطه في إعداد الصفحة للصفحة. الرجاء استخدام[**PageProps.PageWidth**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pageprops#PageWidth)و[**PageProps.PageHeight**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pageprops#PageHeight)خصائص لهذا الغرض.

## **الحصول على عرض الصفحة وارتفاع دعامة الصفحة**

 يشرح نموذج التعليمات البرمجية التالي استخدام[**PageProps.PageWidth**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pageprops#PageWidth)و[**PageProps.PageHeight**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pageprops#PageHeight)الخصائص.

### **عينة من الرموز**


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

