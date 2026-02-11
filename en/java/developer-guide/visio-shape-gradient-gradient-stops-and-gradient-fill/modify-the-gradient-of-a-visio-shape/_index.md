---
title: Modify the Gradient of a Visio Shape
type: docs
weight: 10
url: /java/modify-the-gradient-of-a-visio-shape/
---

{{% alert color="primary" %}} 

Using Aspose.Diagram API, developers can enhance the appearance of a Visio shape by modifying the properties of the gradient. Developers can retrieve a gradient fill to set the direction, angle, gradient stop color and position etc.

{{% /alert %}} 
## **Modify the Gradient Fill Programming Sample**
[Shape](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class offers Fill property which allows developers to retrieve a [GradientFill](https://reference.aspose.com/diagram/java/com.aspose.diagram/gradientfill) object. The GradientFill class holds the gradient data of a Visio Shape. Developers can set all its available properties as well as retrieve a gradient stop by index to set the color and position properties.

```
{{< highlight "java" >}}
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(ModifyShapeGradientFill.class) + "ShapeGradientFill\\";

// load a Visio drawing
Diagram diagram = new Diagram(dataDir + "ShapewithGradientFill.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by ID
Shape shape = page.getShapes().getShape(1);
// get the gradient fill properties
GradientFill gradientfill = shape.getFill().getGradientFill();
// get the gradient stops
GradientStopCollection stops = gradientfill.getGradientStops();
// get the gradient stop by index
GradientStop stop = stops.get(0);
// set gradient stop properties
stop.getColor().getUfe().setF("");
stop.getPosition().setValue(0.5);
gradientfill.getGradientDir().setValue(GradientFillDir.RECTANGLE_FROM_BOTTOM_RIGHT);
gradientfill.getGradientAngle().setValue(0.7853981633974501);
// save the Visio drawing
diagram.save(dataDir + "ShapewithGradientFill_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}
```
