---
title: Convertir una forma Visio a Svg
type: docs
weight: 10
url: /es/net/convert-a-visio-shape-to-svg/
description: Esta sección explica cómo convertir una forma visio a svg con Aspose.Diagram.
---
## ** Convierte una forma visio a svg**
 El método ToSvg expuesto por el[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) La clase se puede usar para convertir a svg.

El siguiente código muestra cómo:

1. Cargue una muestra diagram.
1. obtener una página en particular.
1. obtener una forma particular.
1. convertir forma a svg.
### **Forma a Svg**
Use el siguiente código en su aplicación .net para convertir una forma visio a svg.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToSvg.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

SVGSaveOptions svgOptions = new SVGSaveOptions();
// Shape to Svg
shape.ToSvg("out.svg",svgOptions);

{{< /highlight >}}
```

