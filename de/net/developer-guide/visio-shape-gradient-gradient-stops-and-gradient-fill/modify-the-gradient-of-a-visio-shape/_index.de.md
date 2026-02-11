---
title: Ändern Sie den Farbverlauf einer Visio-Form
type: docs
weight: 10
url: /de/net/modify-the-gradient-of-a-visio-shape/
description: Auf dieser Seite wird beschrieben, wie Sie die Verlaufsfarbe einer visio-Form mit der Aspose.Diagram-Bibliothek ändern.
---
{{% alert color="primary" %}} 

Mit Aspose.Diagram API können Entwickler das Erscheinungsbild einer Visio-Form verbessern, indem sie die Eigenschaften des Farbverlaufs ändern. Entwickler können eine Verlaufsfüllung abrufen, um die Richtung, den Winkel, die Farbe und Position des Verlaufsstopps usw. festzulegen.

{{% /alert %}} 
## **Ändern Sie das Farbverlaufs-Programmierbeispiel**
[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)Die Klasse bietet die Fill-Eigenschaft, mit der Entwickler a abrufen können[GradientFill](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientfill)Objekt. Die GradientFill-Klasse enthält die Verlaufsdaten einer Visio-Form. Entwickler können alle verfügbaren Eigenschaften festlegen sowie einen Gradientenstopp nach Index abrufen, um die Farb- und Positionseigenschaften festzulegen.

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
