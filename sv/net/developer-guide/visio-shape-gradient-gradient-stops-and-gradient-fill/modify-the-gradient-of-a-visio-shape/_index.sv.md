---
title: Ändra gradienten för en Visio-form
type: docs
weight: 10
url: /sv/net/modify-the-gradient-of-a-visio-shape/
description: Den här sidan beskriver hur man ändrar övertoningsfärg för en visio-form med Aspose.Diagram-biblioteket.
---
{{% alert color="primary" %}} 

Med hjälp av Aspose.Diagram API kan utvecklare förbättra utseendet på en Visio form genom att modifiera egenskaperna för gradienten. Utvecklare kan hämta en gradientfyllning för att ställa in riktning, vinkel, gradientstoppfärg och position etc.

{{% /alert %}} 
## **Ändra programmeringsexemplet för gradientfyllning**
[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)class erbjuder Fill-egenskap som gör att utvecklare kan hämta en[GradientFill](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientfill)objekt. Klassen GradientFill innehåller gradientdata för en Visio Shape. Utvecklare kan ställa in alla dess tillgängliga egenskaper samt hämta en gradient stopp för index för att ställa in färg- och positionsegenskaper.

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
