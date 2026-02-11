---
title: Convertir una forma Visio a Svg
type: docs
weight: 10
url: /es/java/convert-a-visio-shape-to-svg/
description: Esta sección explica cómo convertir una forma visio a svg con Aspose.Diagram.
---
## ** Convierte una forma visio a svg**
 El método ToSvg expuesto por el[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) La clase se puede usar para convertir a svg.

El siguiente código muestra cómo:

1. Cargue una muestra diagram.
1. obtener una página en particular.
1. obtener una forma particular.
1. convertir forma a svg.
### **Forma a Svg**
Use el siguiente código en su aplicación java para convertir una forma visio a svg.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ShapeToSvg.class); 
// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToSvg.vsdx");

// Get a particular page
Page page = diagram.getPages().get(0);

// Get a particular shape
Shape shape = page.getShapes().get(0);

// Shape to Svg
SVGSaveOptions option = new SVGSaveOptions();
shape.toSvg("out.svg",option);
{{< /highlight >}}
```


