---
title: Konvertera en Visio Shape till Svg
type: docs
weight: 10
url: /sv/net/convert-a-visio-shape-to-svg/
description: Det här avsnittet förklarar hur man konverterar en visio-form till svg med Aspose.Diagram.
---
## ** Konvertera en visio-form till svg**
 ToSvg-metoden exponerad av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass kan användas för att konvertera till svg.

Koden nedan visar hur man:

1. Ladda ett prov diagram.
1. skaffa en viss sida.
1. få en speciell form.
1. konvertera form till svg.
### **Form till Svg**
Använd följande kod i din .net-applikation för att konvertera en visio-form till svg.


{{< highlight csharp >}}
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


