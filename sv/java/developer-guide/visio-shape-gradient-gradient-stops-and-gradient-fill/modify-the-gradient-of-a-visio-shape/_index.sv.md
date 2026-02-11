---
title: Ändra gradienten för en Visio-form
type: docs
weight: 10
url: /sv/java/modify-the-gradient-of-a-visio-shape/
---
{{% alert color="primary" %}} 

Med hjälp av Aspose.Diagram API kan utvecklare förbättra utseendet på en Visio form genom att modifiera egenskaperna för gradienten. Utvecklare kan hämta en gradientfyllning för att ställa in riktning, vinkel, gradientstoppfärg och position etc.

{{% /alert %}} 
## **Ändra programmeringsexemplet för gradientfyllning**
[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)class erbjuder Fill-egenskap som gör att utvecklare kan hämta en[GradientFill](https://reference.aspose.com/diagram/java/com.aspose.diagram/gradientfill)objekt. Klassen GradientFill innehåller gradientdata för en Visio Shape. Utvecklare kan ställa in alla dess tillgängliga egenskaper samt hämta en gradient stopp för index för att ställa in färg- och positionsegenskaper.

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
