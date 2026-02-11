---
title: Obtenir la largeur du papier et la hauteur de la page
type: docs
weight: 50
url: /fr/java/get-paper-width-and-height-of-page/
description: Cette section explique comment obtenir le format de papier de la page visio avec Aspose.Diagram.
---
## **Scénarios d'utilisation possibles**

Parfois, vous devez connaître la largeur et la hauteur du format de papier tel qu'il a été défini dans la mise en page de la page. Veuillez utiliser le[**PageProps.PageWidthPageProps.PageWidth**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pageprops#PageWidth)et[**PageProps.PageHeightPageProps.PageHeight**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pageprops#PageHeight)propriétés à cet effet.

## **Obtenir la largeur et la hauteur de la page Prop de la page**

 L'exemple de code suivant explique l'utilisation de[**PageProps.PageWidthPageProps.PageWidth**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pageprops#PageWidth)et[**PageProps.PageHeightPageProps.PageHeight**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pageprops#PageHeight)Propriétés.

### **Exemple de code**


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

