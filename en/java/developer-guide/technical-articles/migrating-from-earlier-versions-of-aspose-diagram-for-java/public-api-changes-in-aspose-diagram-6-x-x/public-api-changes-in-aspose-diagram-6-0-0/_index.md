---
title: Public API Changes in Aspose.Diagram 6.0.0
type: docs
weight: 50
url: /java/public-api-changes-in-aspose-diagram-6-0-0/
---

{{% alert color="primary" %}} 

This document describes changes to the Aspose.Diagram API from version 5.9.0 to 6.0.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behaviour behind the scenes in Aspose.Diagram. 

{{% /alert %}} 
### **isGlued Method is added in the Shape class**
The isGlued method takes a shape object as a parameter to determine that the two shapes glued or not. 
Example code:

**Java**

{{< highlight java >}}

 // Call the diagram constructor to load diagram

Diagram diagram = new Diagram("C:/temp/Drawing1.vsdx");

// get Visio page by name

Page page = diagram.getPages().getPage("Page-1");

// get Visio shapes by ids

Shape ShapedOne = page.getShapes().getShape(1);

Shape ShapedTwo = page.getShapes().getShape(2);

// determine whether shapes are glued

boolean glued = ShapedOne.isGlued(ShapedTwo);

{{< /highlight >}}
### **isConnected Method is added in the Shape class**
The isConnected method takes a shape object as a parameter to determine that the two shapes connected or not.
Example code:

**Java**

{{< highlight java >}}

 // Call the diagram constructor to load diagram

Diagram diagram = new Diagram("C:/temp/Drawing1.vsdx");

// get Visio page by name

Page page = diagram.getPages().getPage("Page-1");

// get Visio shapes by ids

Shape ShapedOne = page.getShapes().getShape(1);

Shape ShapedTwo = page.getShapes().getShape(2);

// determine whether shapes are connected

boolean connected = ShapedOne.isConnected(ShapedTwo);

{{< /highlight >}}
