---
title: Ottieni la larghezza della carta e l'altezza della pagina
type: docs
weight: 50
url: /it/java/get-paper-width-and-height-of-page/
description: Questa sezione spiega come ottenere il formato carta della pagina visio con Aspose.Diagram.
---
## **Possibili scenari di utilizzo**

A volte, è necessario conoscere la larghezza e l'altezza del formato carta poiché è stata impostata nell'impostazione della pagina della pagina. Si prega di utilizzare il[**PageProps.PageWidth**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pageprops#PageWidth)e[**PageProps.PageHeight**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pageprops#PageHeight)proprietà a questo scopo.

## **Ottieni la larghezza e l'altezza della pagina Prop della pagina**

 Il seguente codice di esempio spiega l'utilizzo di[**PageProps.PageWidth**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pageprops#PageWidth)e[**PageProps.PageHeight**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pageprops#PageHeight)proprietà.

### **Codice di esempio**


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

