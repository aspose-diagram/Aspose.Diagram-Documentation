---
title: Public API Changes in Aspose.Diagram 6.0.0
type: docs
weight: 40
url: /net/public-api-changes-in-aspose-diagram-6-0-0/
---

{{% alert color="primary" %}} 

This document describes changes to the Aspose.Diagram API from version 5.9.0 to 6.0.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.Diagram.

{{% /alert %}} 
## **IsGlued Method is added in the Shape class**
The IsGlued method takes a shape object as a parameter to determine that the two shapes glued or not. 
Example code:

**C#**

{{< highlight java >}}

 // Call the diagram constructor to load diagram

Diagram diagram = new Diagram("C:/temp/Drawing1.vsdx");

// get Visio page by name

Page page = diagram.Pages.GetPage("Page-1");

// get Visio shapes by ids

Shape ShapedOne = page.Shapes.GetShape(1);

Shape ShapedTwo = page.Shapes.GetShape(2);

// determine whether shapes are glued

bool glued = ShapedOne.IsGlued(ShapedTwo);

{{< /highlight >}}

**VB**

{{< highlight java >}}

 ' Call the diagram constructor to load diagram

Dim diagram As New Diagram("C:/temp/Drawing1.vsdx")

' get Visio page by name

Dim page As Page = diagram.Pages.GetPage("Page-1")

' get Visio shapes by ids

Dim ShapedOne As Shape = page.Shapes.GetShape(1)

Dim ShapedTwo As Shape = page.Shapes.GetShape(2)

' determine whether shapes are glued

Dim glued As Boolean = ShapedOne.IsGlued(ShapedTwo)

{{< /highlight >}}
## **IsConnected Method is added in the Shape class**
The IsConnected method takes a shape object as a parameter to determine that the two shapes connected or not.
Example code:

**C#**

{{< highlight java >}}

 // Call the diagram constructor to load diagram

Diagram diagram = new Diagram("C:/temp/Drawing1.vsdx");

// get Visio page by name

Page page = diagram.Pages.GetPage("Page-1");

// get Visio shapes by ids

Shape ShapedOne = page.Shapes.GetShape(1);

Shape ShapedTwo = page.Shapes.GetShape(2);

// determine whether shapes are glued

bool glued = ShapedOne.IsConnected(ShapedTwo);

{{< /highlight >}}

**VB**

{{< highlight java >}}

 ' Call the diagram constructor to load diagram

Dim diagram As New Diagram("C:/temp/Drawing1.vsdx")

' get Visio page by name

Dim page As Page = diagram.Pages.GetPage("Page-1")

' get Visio shapes by ids

Dim ShapedOne As Shape = page.Shapes.GetShape(1)

Dim ShapedTwo As Shape = page.Shapes.GetShape(2)

' determine whether shapes are glued

Dim glued As Boolean = ShapedOne.IsConnected(ShapedTwo)

{{< /highlight >}}
