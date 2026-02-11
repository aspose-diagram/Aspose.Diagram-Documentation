---
title: Manipulate the Embedded OLE Objects in Visio Diagram
type: docs
weight: 10
url: /java/manipulate-the-embedded-ole-objects-in-visio-diagram/
description: This page describes how to manipulate ole object with Aspose.Diagram library.
---

{{% alert color="primary" %}}

Microsoft Office Visio supports manipulating the OLE objects in the Visio diagram. If an visio file resides outside of the Visio drawing and developers need to add a feature in their Java applications to auto insert these files inside of the drawing, they can achieve this by using [Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

{{% /alert %}}
## **Manipulate the Embedded OLE Objects Programming Sample**
[ObjectData](https://reference.aspose.com/diagram/java/com.aspose.diagram/foreigndata#ObjectData) property of the [ForeignData](https://reference.aspose.com/diagram/java/com.aspose.diagram/foreigndata) class allows developers to manipulate with existing OLE objects in Visio diagram. This help topic demonstrates how developers can retrieve an OLE object of the Visio document, edit it using [Aspose.Diagram for Java API](https://products.aspose.com/diagram/java), and then save back as an OLE object in the Visio diagram.


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

