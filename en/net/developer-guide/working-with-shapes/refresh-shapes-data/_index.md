---
title: Refresh shapes data
type: docs
weight: 40
url: /net/refresh-shapes-data/
description: This section explains how to refresh shape's data for a visio shape with Aspose.Diagram.
---

## **Refreshes shape's position including xform ,connection and geom when changing shape's text or other's **
The RefreshData method exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class can be used to refresh shape's data

The code below shows how to:

1. Load a sample file.
1. Access a particular shape.
1. Refresh shape's data.
### **Refresh Shape's data**
Use the following code in your .NET application to refresh a shape using Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

// Get Shape
Shape shape = page.Shapes.GetShape(15);

// Refresh data
shape.RefreshData();

// Save visio diagram
diagram.Save(dataDir + "RefreshData_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


