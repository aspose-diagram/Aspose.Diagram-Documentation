---
title: Recuperar un control ActiveX de un objeto de forma para modificar propiedades
type: docs
weight: 20
url: /es/java/retrieve-an-activex-control-from-a-shape-object-to-modify-properties/
---
{{% alert color="primary" %}} 

Con Aspose.Diagram API, los desarrolladores pueden recuperar un control ActiveX de un objeto de forma Visio para configurar todas sus propiedades disponibles.

{{% /alert %}} 
## **Recuperar una muestra de programación de control ActiveX**
[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) La clase ofrece el método getActiveXControl que permite a los desarrolladores recuperar un control ActiveX de un objeto de forma Visio. Los desarrolladores pueden convertir un control ActiveX en la clase de control ActiveX adecuada y luego establecer todas sus propiedades disponibles.

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
