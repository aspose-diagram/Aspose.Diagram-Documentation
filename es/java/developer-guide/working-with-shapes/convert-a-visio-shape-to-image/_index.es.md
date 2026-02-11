---
title: Convertir una forma Visio en imagen
type: docs
weight: 10
url: /es/java/convert-a-visio-shape-to-image/
description: Esta sección explica cómo convertir una forma visio en una imagen con Aspose.Diagram.
---
## **Convierte una forma visio en imagen**
 El método ToImage expuesto por el[Forma](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) La clase se puede utilizar para convertir a imagen.

El siguiente código muestra cómo:

1. Cargue una muestra diagram.
1. obtener una página en particular.
1. obtener una forma particular.
1. convertir forma en imagen.
### **Forma a imagen**
Use el siguiente código en su aplicación Java para convertir una forma visio en una imagen.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ShapeToImage.class); 
// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToImage.vsdx");

// Get a particular page
Page page = diagram.getPages().get(0);

// Get a particular shape
Shape shape = page.getShapes().get(0);

// Shape to image
com.aspose.diagram.ImageSaveOptions option = new com.aspose.diagram.ImageSaveOptions(SaveFileFormat.PNG);
shape.toImage("out.png",option);
{{< /highlight >}}
```


