---
title: Convertir una forma Visio en imagen
type: docs
weight: 10
url: /es/net/convert-a-visio-shape-to-image/
description: Esta sección explica cómo convertir una forma visio en una imagen con Aspose.Diagram.
---
## **Convierte una forma visio en imagen**
Este tema explica cómo los desarrolladores pueden convertir una forma visio en una imagen usando Aspose.Diagram.
 El método ToImage expuesto por el[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) La clase se puede utilizar para convertir a imagen.


El siguiente código muestra cómo:

1. Cargue una muestra diagram.
1. obtener una página en particular.
1. obtener una forma particular.
1. convertir forma en imagen.
#### **Muestra de programación de forma a imagen**
Use el siguiente código en su aplicación .net para convertir una forma visio en una imagen.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToImage.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

// Shape to Image
Aspose.Diagram.Saving.ImageSaveOptions o = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);
shape.ToImage("out.png", o);

{{< /highlight >}}
```
