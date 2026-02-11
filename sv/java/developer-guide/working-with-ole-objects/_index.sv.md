---
title: Arbeta med OLE-objekt
type: docs
weight: 220
url: /sv/java/working-with-ole-objects/
---
{{% alert color="primary" %}}

Microsoft Office Visio stöder manipulering av OLE-objekten i Visio diagram. Om ett Excel-kalkylblad eller någon annan fil finns utanför Visio-ritningen och utvecklarna i deras 3406 applikationer måste lägga till 3406 inuti en automatisk applikation. uppnå detta genom att använda[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

{{% /alert %}}
### **Manipulera programmeringsexemplet för inbäddade OLE-objekt**
 ObjectData-egenskapen i klassen ForeignData tillåter utvecklare att manipulera med befintliga OLE-objekt i Visio diagram. Det här hjälpämnet visar hur utvecklare kan hämta ett OLE-objekt i Word-dokumentet, redigera det med hjälp av[Aspose.Words for Java API](https://products.aspose.com/words/java), och spara sedan tillbaka som ett OLE-objekt i Visio diagram.

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
