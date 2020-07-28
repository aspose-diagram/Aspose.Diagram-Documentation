+++
title = "Public API Changes in Aspose.Diagram 16.12.0" 
description = "" 
weight = 20071 
+++

Aspose.Diagram for Java : Public API Changes in Aspose.Diagram 16.12.0  

# Aspose.Diagram for Java : Public API Changes in Aspose.Diagram 16.12.0


This document describes changes to the Aspose.Diagram API from version 16.11.0 to 16.12.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behaviour behind the scenes in Aspose.Diagram.

### Modify Properties of a Gradient

Developers can retrieve a gradient stop and then modify its properties. We have added [GradientFill](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientfill) and [GradientStop](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientstop) classes for this purposes. Please check the code example:

**Java**

{{< code lang="java" >}}
// load a Visio drawing
Diagram diagram = new Diagram("C:\\temp\\MyVisio.vsdx");
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
diagram.save("C:\\temp\\Output.pdf", SaveFileFormat.PDF);
{{< /code >}}

