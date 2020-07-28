+++
title = "Public API Changes in Aspose.Diagram 5.8.0" 
description = "" 
weight = 20079 
+++

Aspose.Diagram for .NET : Public API Changes in Aspose.Diagram 5.8.0  

# Aspose.Diagram for .NET : Public API Changes in Aspose.Diagram 5.8.0


This document describes changes to the Aspose.Diagram API from version 5.7.0 to 5.8.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.Diagram.

### SaveToolBar Option is added in the HTMLSaveOptions 

The new SaveToolBar option has been added in the HTMLSaveOptions class. It specifies whether to save toolbar or not. The default value is true. Example codes:

**C#**

{{< code lang="c#" >}}
// initialize HTMLSaveOptions class object
HTMLSaveOptions opts = new HTMLSaveOptions();

// set save toolbar option
opts.SaveToolBar = false;
{{< /code >}}

**VB**

{{< code lang="vb" >}}
' initialize HTMLSaveOptions class object
Dim opts As New HTMLSaveOptions()

' set save toolbar option
opts.SaveToolBar = False
{{< /code >}}

### VSDX Saving Option is added in the SaveFileFormat 

Previously, Aspose.Diagram API supported reading VSDX format, but now we have added support of writing diagrams in the VSDX format. Example codes:

**C#**

{{< code lang="c#" >}}
// save diagram in the VSDX format
diagram.Save("C:\\temp\\Output.vsdx", SaveFileFormat.VSDX);
{{< /code >}}

**VB**

{{< code lang="vb" >}}
' save diagram in the VSDX format
diagram.Save("C:\temp\Output.vsdx", SaveFileFormat.VSDX)
{{< /code >}}

### Group Method has been added in the ShapeCollection Class

Developers can now group multiple shapes together in the Visio diagram using Aspose.Diagram API. Example codes:

**C#**

{{< code lang="c#" >}}
// load a Visio diagram
Diagram diagram = new Diagram(@"c:\temp\test.vdx");

// Initialize an array of shapes
Aspose.Diagram.Shape[] ss = new Aspose.Diagram.Shape[2];

// extract and assign shapes to the array
ss[0] = diagram.Pages[0].Shapes.GetShape(1);
ss[1] = diagram.Pages[0].Shapes.GetShape(2);

// mark array shapes as group
diagram.Pages[0].Shapes.Group(ss);

// save visio diagram
diagram.Save(@"c:\temp\out.vsdx", SaveFileFormat.VSDX);
{{< /code >}}

**VB**

{{< code lang="vb" >}}
' load a Visio diagram
Dim diagram As New Diagram("c:\temp\test.vdx")

' Initialize an array of shapes
Dim ss As Aspose.Diagram.Shape() = New Aspose.Diagram.Shape(1) {}

' extract and assign shapes to the array
ss(0) = diagram.Pages(0).Shapes.GetShape(1)
ss(1) = diagram.Pages(0).Shapes.GetShape(2)

' mark array shapes as group
diagram.Pages(0).Shapes.Group(ss)

' save visio diagram
diagram.Save("c:\temp\out.vsdx", SaveFileFormat.VSDX)
{{< /code >}}

