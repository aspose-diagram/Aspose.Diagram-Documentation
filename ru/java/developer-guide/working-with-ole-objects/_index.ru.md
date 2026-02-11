---
title: Работа с OLE-объектами
type: docs
weight: 220
url: /ru/java/working-with-ole-objects/
---
{{% alert color="primary" %}}

Microsoft Office Visio поддерживает управление объектами OLE в Visio diagram. Если электронная таблица Excel или любой другой файл находится за пределами чертежа Visio и разработчикам необходимо добавить функцию в свои приложения Java для автоматической вставки этих файлов внутрь чертежа, они могут достичь этого с помощью[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

{{% /alert %}}
### **Управление примером программирования встроенных объектов OLE**
 Свойство ObjectData класса ForeignData позволяет разработчикам манипулировать существующими объектами OLE в Visio diagram. В этом разделе справки показано, как разработчики могут получить объект OLE документа Word, отредактировать его с помощью[Aspose.Words for Java API](https://products.aspose.com/words/java), а затем сохраните обратно как объект OLE в файле Visio diagram.


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

