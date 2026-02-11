---
title: Convert a Visio Shape To Svg
type: docs
weight: 10
url: /net/convert-a-visio-shape-to-svg/
description: This section explains how to convert a visio shape to svg with Aspose.Diagram.
---

## **Convert a visio shape to svg **
The ToSvg method exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class can be used to convert to svg.

The code below shows how to:

1. Load a sample diagram.
1. get a particular page.
1. get a particular shape.
1. convert shape to svg.
### **Shape to Svg**
Use the following code in your .net application to convert a visio shape to svg.


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


