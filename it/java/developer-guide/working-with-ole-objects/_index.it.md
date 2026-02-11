---
title: Lavorare con oggetti OLE
type: docs
weight: 220
url: /it/java/working-with-ole-objects/
---
{{% alert color="primary" %}}

Microsoft Office Visio supporta la manipolazione degli oggetti OLE nel Visio diagram. Se un foglio di calcolo Excel o qualsiasi altro file risiede al di fuori del disegno Visio e gli sviluppatori devono aggiungere una funzione nelle loro applicazioni Java per inserire automaticamente questi file all'interno del disegno, possono raggiungere questo obiettivo utilizzando[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

{{% /alert %}}
### **Manipolare l'esempio di programmazione di oggetti OLE incorporati**
 La proprietà ObjectData della classe ForeignData consente agli sviluppatori di manipolare oggetti OLE esistenti in Visio diagram. Questo argomento della guida illustra come gli sviluppatori possono recuperare un oggetto OLE del documento Word, modificarlo utilizzando[Aspose.Words for Java API](https://products.aspose.com/words/java), quindi salvare di nuovo come oggetto OLE in Visio diagram.


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

