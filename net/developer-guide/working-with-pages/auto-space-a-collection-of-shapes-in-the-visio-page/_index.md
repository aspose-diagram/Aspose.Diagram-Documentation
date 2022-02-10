---
title: Auto-space a Collection of Shapes in the Visio Page
type: docs
weight: 30
url: /net/auto-space-a-collection-of-shapes-in-the-visio-page/
description: This section explains how to autospace a collection of shapes in a visio page with Aspose.Diagram.
---

## **Auto-space a Collection of Shapes in the Visio Page**
With Aspose.Diagram for .NET API, developers can auto-space a collection of shapes in the Visio drawing. In order to achieve this, the Page class offers AutoSpaceShapes member which takes ShapeCollection and AutoSpaceOptions parameters. The AutoSpaceOptions class allows to set horizontal and vertical distances.
### **Auto-space Shapes in the Page**
Use the following code in your .NET application to auto-space a collection of shapes in any page of the Visio drawing.

**C#**

{{< highlight java >}}

 // load a Visio drawing

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// get page of the Visio drawing

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// initialize auto space options

AutoSpaceOptions options = new AutoSpaceOptions();

// set horizontal and vertical distances

options.DistanceInHorizontal = 2;

options.DistanceInVertical = 2;

// set auto space 

page.AutoSpaceShapes(page.Shapes, options);

// save Visio drawing

diagram.Save(@"c:\temp\AutoSpaceShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
