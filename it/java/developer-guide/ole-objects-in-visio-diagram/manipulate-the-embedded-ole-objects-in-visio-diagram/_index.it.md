---
title: Manipolare gli oggetti OLE incorporati in Visio Diagram
type: docs
weight: 10
url: /it/java/manipulate-the-embedded-ole-objects-in-visio-diagram/
description: Questa pagina descrive come manipolare un oggetto ole con la libreria Aspose.Diagram.
---
{{% alert color="primary" %}}

Microsoft Office Visio supporta la manipolazione degli oggetti OLE nel disegno Visio diagram.[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

{{% /alert %}}
## **Manipolare l'esempio di programmazione di oggetti OLE incorporati**
[ObjectData](https://reference.aspose.com/diagram/java/com.aspose.diagram/foreigndata#ObjectData) proprietà del[Dati Esteri](https://reference.aspose.com/diagram/java/com.aspose.diagram/foreigndata) consente agli sviluppatori di manipolare oggetti OLE esistenti in Visio diagram. Questo argomento della guida mostra come gli sviluppatori possono recuperare un oggetto OLE del documento Visio, modificarlo utilizzando[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java), quindi salvare di nuovo come oggetto OLE in Visio diagram.


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

