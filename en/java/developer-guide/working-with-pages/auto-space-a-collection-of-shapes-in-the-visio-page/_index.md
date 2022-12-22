---
title: Auto-space a Collection of Shapes in the Visio Page
type: docs
weight: 30
url: /java/auto-space-a-collection-of-shapes-in-the-visio-page/
---

## **Auto-space a Collection of Shapes in the Visio Page**
With Aspose.Diagram for Java API, developers can auto-space a collection of shapes in the Visio drawing. In order to achieve this, the Page class offers autoSpaceShapes member which takes ShapeCollection and AutoSpaceOptions parameters. The AutoSpaceOptions class allows to set horizontal and vertical distances.
### **Auto-space Shapes in the Page**
Use the following code in your Java application to auto-space a collection of shapes in any page of the Visio drawing.

**Java**

{{< highlight java >}}

 // load a Visio drawing

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// get page of the Visio drawing

Page page = diagram.getPages().getPage("Page-1");

// initialize auto space options

AutoSpaceOptions options = new AutoSpaceOptions();

// set horizontal and vertical distances

options.setDistanceInHorizontal(2);

options.setDistanceInVertical(2);

// set auto space 

page.autoSpaceShapes(page.getShapes(), options);

// save Visio drawing

diagram.save("c:\\temp\\AutoSpaceShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
