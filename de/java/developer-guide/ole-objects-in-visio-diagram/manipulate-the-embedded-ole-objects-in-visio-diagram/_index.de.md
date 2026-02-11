---
title: Bearbeiten Sie die eingebetteten OLE-Objekte in Visio Diagram
type: docs
weight: 10
url: /de/java/manipulate-the-embedded-ole-objects-in-visio-diagram/
description: Diese Seite beschreibt, wie man ein Ole-Objekt mit der Bibliothek Aspose.Diagram manipuliert.
---
{{% alert color="primary" %}}

Microsoft Office Visio unterstützt die Bearbeitung der OLE-Objekte in Visio diagram. Wenn sich eine visio-Datei außerhalb der Visio-Zeichnung befindet und Entwickler eine Funktion in ihren Java-Anwendungen hinzufügen müssen, um diese Dateien automatisch in die Zeichnung einzufügen, können sie dies erreichen, indem sie verwenden[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

{{% /alert %}}
## **Bearbeiten Sie das Programmierbeispiel für eingebettete OLE-Objekte**
[Objektdaten](https://reference.aspose.com/diagram/java/com.aspose.diagram/foreigndata#ObjectData) Eigentum der[Ausländische Daten](https://reference.aspose.com/diagram/java/com.aspose.diagram/foreigndata) -Klasse ermöglicht es Entwicklern, vorhandene OLE-Objekte in Visio diagram zu manipulieren. Dieses Hilfethema zeigt, wie Entwickler ein OLE-Objekt des Visio-Dokuments abrufen und bearbeiten können[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java), und speichern Sie sie dann als OLE-Objekt in Visio diagram zurück.


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

