---
title: Public API Changes in Aspose.Diagram 16.12.0
type: docs
weight: 10
url: /net/public-api-changes-in-aspose-diagram-16-12-0/
---

{{% alert color="primary" %}} 

This document describes changes to the Aspose.Diagram API from version 16.11.0 to 16.12.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.Diagram.

{{% /alert %}} 
## **Modify Properties of a Gradient**
Developers can retrieve a gradient stop and then modify its properties. We have added [GradientFill](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientfill) and [GradientStop](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientstop) classes for this purposes. Please check the code example:

**C#**

{{< highlight csharp >}}

 // load a Visio drawing

Diagram diagram = new Diagram(@"C:\temp\MyVisio.vsdx");

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

diagram.Save(@"C:\temp\Output.pdf", SaveFileFormat.PDF);

{{< /highlight >}}
