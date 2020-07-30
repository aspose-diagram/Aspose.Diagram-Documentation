---
title : "Public API Changes in Aspose.Diagram 16.11.0" 
description : "" 
weight : 20072 
toc : false
type: docs
url: /java/developerguide/knowledgebase/migratingfromearliervs/changesin16xx/public+api+changes+in+aspose.diagram+16.11.0/
---

# Aspose.Diagram for Java : Public API Changes in Aspose.Diagram 16.11.0


This document describes changes to the Aspose.Diagram API from version 6.8.0 to 16.11.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behaviour behind the scenes in Aspose.Diagram.

### Modify Properties of an ActiveX Control

Developers can retrieve an ActiveX control and then modify its properties. We have added `ActiveXControl` property in the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class. Please check this code example:

**Java**

{{< code lang="java" >}}
// load a Visio diagram
Diagram diagram = new Diagram("C:\\temp\\Drawing1.vsd");
// get a Visio page by name
Page page = diagram.getPages().getPage("Page-1");
// get a shape by ID
Shape shape = page.getShapes().getShape(1);
// get an ActiveX control
CommandButtonActiveXControl cbac = (CommandButtonActiveXControl)shape.getActiveXControl();
// set width of the command button control
cbac.setWidth(4);
// set height of the command button control
cbac.setHeight(4);
// set caption of the command button control
cbac.setCaption("Test Button");
// save diagram
diagram.save("C:\\temp\\Output.vsdx", SaveFileFormat.VSDX);
{{< /code >}}

### Insert a Text Shape in the Visio Diagram

Developers can insert a text shape in the Visio diagram using Aspose.Diagram API. Please check this code example:

**C#**

{{< code lang="c#" >}}
// create a new diagram
Diagram diagram = new Diagram();
// set parameters
double PinX = 1, PinY = 1, Width = 1, Height = 1;
String text = "Test text";
// add text to a Visio page
diagram.getPages().get(0).addText(PinX, PinY, Width, Height, text);
// save diagram 
diagram.save("C:\\temp\\Output.vsdx", SaveFileFormat.VSDX);
{{< /code >}}

