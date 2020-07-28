+++
title = "Public API Changes in Aspose.Diagram 6.0.0" 
description = "" 
weight = 20076 
+++

Aspose.Diagram for .NET : Public API Changes in Aspose.Diagram 6.0.0  

# Aspose.Diagram for .NET : Public API Changes in Aspose.Diagram 6.0.0


This document describes changes to the Aspose.Diagram API from version 5.9.0 to 6.0.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.Diagram.

### IsGlued Method is added in the Shape class

The IsGlued method takes a shape object as a parameter to determine that the two shapes glued or not.   
Example code:

**C#**

{{< code lang="c#" >}}
// Call the diagram constructor to load diagram
Diagram diagram = new Diagram("C:/temp/Drawing1.vsdx");

// get Visio page by name
Page page = diagram.Pages.GetPage("Page-1");

// get Visio shapes by ids
Shape ShapedOne = page.Shapes.GetShape(1);
Shape ShapedTwo = page.Shapes.GetShape(2);

// determine whether shapes are glued
bool glued = ShapedOne.IsGlued(ShapedTwo);
{{< /code >}}

**VB**

{{< code lang="vb" >}}
' Call the diagram constructor to load diagram
Dim diagram As New Diagram("C:/temp/Drawing1.vsdx")

' get Visio page by name
Dim page As Page = diagram.Pages.GetPage("Page-1")

' get Visio shapes by ids
Dim ShapedOne As Shape = page.Shapes.GetShape(1)
Dim ShapedTwo As Shape = page.Shapes.GetShape(2)

' determine whether shapes are glued
Dim glued As Boolean = ShapedOne.IsGlued(ShapedTwo)
{{< /code >}}

### IsConnected Method is added in the Shape class

The IsConnected method takes a shape object as a parameter to determine that the two shapes connected or not.  
Example code:

**C#**

{{< code lang="c#" >}}
// Call the diagram constructor to load diagram
Diagram diagram = new Diagram("C:/temp/Drawing1.vsdx");

// get Visio page by name
Page page = diagram.Pages.GetPage("Page-1");

// get Visio shapes by ids
Shape ShapedOne = page.Shapes.GetShape(1);
Shape ShapedTwo = page.Shapes.GetShape(2);

// determine whether shapes are glued
bool glued = ShapedOne.IsConnected(ShapedTwo);
{{< /code >}}

**VB**

{{< code lang="vb" >}}
' Call the diagram constructor to load diagram
Dim diagram As New Diagram("C:/temp/Drawing1.vsdx")

' get Visio page by name
Dim page As Page = diagram.Pages.GetPage("Page-1")

' get Visio shapes by ids
Dim ShapedOne As Shape = page.Shapes.GetShape(1)
Dim ShapedTwo As Shape = page.Shapes.GetShape(2)

' determine whether shapes are glued
Dim glued As Boolean = ShapedOne.IsConnected(ShapedTwo)
{{< /code >}}

