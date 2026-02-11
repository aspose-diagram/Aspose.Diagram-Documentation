---
title: Trabajar con objetos OLE
type: docs
weight: 220
url: /es/java/working-with-ole-objects/
---
{{% alert color="primary" %}}

Microsoft Office Visio admite la manipulación de objetos OLE en Visio diagram. Si una hoja de cálculo de Excel o cualquier otro archivo reside fuera del dibujo Visio y los desarrolladores necesitan agregar una función en sus aplicaciones Java para insertar automáticamente estos archivos dentro del dibujo, pueden lograr esto usando[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

{{% /alert %}}
### **Manipular el ejemplo de programación de objetos OLE incrustados**
 La propiedad ObjectData de la clase ForeignData permite a los desarrolladores manipular objetos OLE existentes en Visio diagram. Este tema de ayuda demuestra cómo los desarrolladores pueden recuperar un objeto OLE del documento de Word, editarlo usando[Aspose.Words for Java API](https://products.aspose.com/words/java)y luego guárdelo como un objeto OLE en el Visio diagram.


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

