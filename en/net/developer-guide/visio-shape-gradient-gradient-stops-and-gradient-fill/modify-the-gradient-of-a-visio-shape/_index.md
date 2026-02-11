---
title: Modify the Gradient of a Visio Shape
type: docs
weight: 10
url: /net/modify-the-gradient-of-a-visio-shape/
description: This page describes how to modify gradient color of a visio shape with Aspose.Diagram library.
---

{{% alert color="primary" %}} 

Using Aspose.Diagram API, developers can enhance the appearance of a Visio shape by modifying the properties of the gradient. Developers can retrieve a gradient fill to set the direction, angle, gradient stop color and position etc.

{{% /alert %}} 
## **Modify the Gradient Fill Programming Sample**
[Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class offers Fill property which allows developers to retrieve a [GradientFill](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientfill) object. The GradientFill class holds the gradient data of a Visio Shape. Developers can set all its available properties as well as retrieve a gradient stop by index to set the color and position properties.

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
