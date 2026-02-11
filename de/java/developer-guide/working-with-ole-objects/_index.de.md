---
title: Arbeiten mit OLE-Objekten
type: docs
weight: 220
url: /de/java/working-with-ole-objects/
---
{{% alert color="primary" %}}

Microsoft Office Visio unterstützt die Bearbeitung der OLE-Objekte in Visio diagram. Wenn sich eine Excel-Tabelle oder eine andere Datei außerhalb der Visio Zeichnung befindet und Entwickler eine Funktion in ihren Java Anwendungen hinzufügen müssen, um diese Dateien automatisch in die Zeichnung einzufügen, können sie dies tun erreichen Sie dies durch die Verwendung[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

{{% /alert %}}
### **Bearbeiten Sie das Programmierbeispiel für eingebettete OLE-Objekte**
 Die ObjectData-Eigenschaft der ForeignData-Klasse ermöglicht es Entwicklern, mit vorhandenen OLE-Objekten in Visio diagram zu arbeiten. Dieses Hilfethema zeigt, wie Entwickler ein OLE-Objekt des Word-Dokuments abrufen und bearbeiten können[Aspose.Words for Java API](https://products.aspose.com/words/java), und speichern Sie sie dann als OLE-Objekt in Visio diagram zurück.

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
