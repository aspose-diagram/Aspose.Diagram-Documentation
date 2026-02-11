---
title: Hämta en ActiveX-kontroll från ett Shape-objekt för att ändra egenskaper
type: docs
weight: 20
url: /sv/java/retrieve-an-activex-control-from-a-shape-object-to-modify-properties/
---
{{% alert color="primary" %}} 

Med hjälp av Aspose.Diagram API kan utvecklare hämta en ActiveX-kontroll från ett Visio-formobjekt för att ställa in alla tillgängliga egenskaper.

{{% /alert %}} 
## **Hämta ett ActiveX-kontrollprogrammeringsexempel**
[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class erbjuder getActiveXControl-metoden som gör att utvecklare kan hämta en ActiveX-kontroll från ett Visio-formobjekt. Utvecklare kan casta en ActiveX-kontroll i lämplig ActiveX-kontrollklass och sedan ställa in dess alla tillgängliga egenskaper.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveActiveXControl.class) + "VisioActiveXControls/";
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");
// get a Visio page by name
Page page = diagram.getPages().getPage("Page-1");
// get a shape by ID
Shape shape = page.getShapes().getShape(1);
// get an ActiveX control
CommandButtonActiveXControl cbac = (CommandButtonActiveXControl)shape.getActiveXControl();
// set width of the command button control
cbac.setWidth(4);
// set height of the command button control
cbac.setHeight(4);
// set caption of the command button control
cbac.setCaption("Test Button");
// save diagram
diagram.save(dataDir + "RetrieveActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
