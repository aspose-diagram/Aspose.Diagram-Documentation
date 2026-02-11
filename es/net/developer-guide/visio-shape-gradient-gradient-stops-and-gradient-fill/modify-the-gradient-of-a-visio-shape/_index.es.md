---
title: Modificar el degradado de una forma Visio
type: docs
weight: 10
url: /es/net/modify-the-gradient-of-a-visio-shape/
description: Esta página describe cómo modificar el color degradado de una forma visio con la biblioteca Aspose.Diagram.
---
{{% alert color="primary" %}} 

Con Aspose.Diagram API, los desarrolladores pueden mejorar la apariencia de una forma Visio modificando las propiedades del degradado. Los desarrolladores pueden recuperar un relleno degradado para establecer la dirección, el ángulo, el color y la posición de parada del degradado, etc.

{{% /alert %}} 
## **Modificar el ejemplo de programación de relleno de degradado**
[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)class ofrece la propiedad Fill que permite a los desarrolladores recuperar un[Relleno degradado](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientfill)objeto. La clase GradientFill contiene los datos de degradado de una forma Visio. Los desarrolladores pueden establecer todas sus propiedades disponibles, así como recuperar un degradado por índice para establecer las propiedades de color y posición.

```
{{< highlight "csharp" >}}
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeGradientFillData();
// Load the Visio diagram
Diagram diagram = new Diagram(dataDir + "ShapewithGradientFill.vsdx");
// get page by name
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");
// get shape by ID
Aspose.Diagram.Shape shape = page.Shapes.GetShape(1);
// get the gradient fill properties
GradientFill gradientfill = shape.Fill.GradientFill;
// get the gradient stops
GradientStopCollection stops = gradientfill.GradientStops;
// get the gradient stop by index
GradientStop stop = stops[0];
// set gradient stop properties
stop.Color.Ufe.F = "";
stop.Position.Value = 0.5;
gradientfill.GradientDir.Value = (int)GradientFillDir.RectangleFromBottomRight;
gradientfill.GradientAngle.Value = 0.7853981633974501;
// save the Visio drawing
diagram.Save(dataDir + "ShapewithGradientFill_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
