---
title: Travailler avec des objets OLE
type: docs
weight: 220
url: /fr/java/working-with-ole-objects/
---
{{% alert color="primary" %}}

Microsoft Office Visio prend en charge la manipulation des objets OLE dans le Visio diagram. Si une feuille de calcul Excel ou tout autre fichier réside en dehors du dessin Visio et que les développeurs doivent ajouter une fonctionnalité dans leurs applications Java pour insérer automatiquement ces fichiers dans le dessin, ils peuvent y parvenir en utilisant[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

{{% /alert %}}
### **Manipuler l'exemple de programmation d'objets OLE intégrés**
 La propriété ObjectData de la classe ForeignData permet aux développeurs de manipuler des objets OLE existants dans Visio diagram. Cette rubrique d'aide montre comment les développeurs peuvent récupérer un objet OLE du document Word, le modifier à l'aide[Aspose.Words for Java API](https://products.aspose.com/words/java), puis enregistrez-le en tant qu'objet OLE dans le fichier Visio diagram.


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

