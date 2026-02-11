---
title: Get Visio Shape Including Child
type: docs
weight: 110
url: /net/get-visio-shape-including-child/
description: This section explains how to get visio shape including child with shape's id or name with Aspose.Diagram.
---
### **Retrieve a Visio Shape Including Child**
Each shape in a diagram has an ID and a name. The ID is important when programming with Visio: it is the main method for accessing a shape. Each shape also retains information about what master (stencil) it is made from.

A [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) is an object in a Visio drawing which possibly hava a father or sons. The Shapes property, exposed by the Page class, supports a collection of Aspose.Diagram.Shape objects. The Shapes property can be used to retrieve information about a shape.
#### **Retrieve Visio Shape Programming Sample**
The following code snippet retrieve the shape including child. Please check this sample code:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "NetworkConnection.vsdx");

Page page = diagram.Pages[0];

Shape shapeContainerChild = page.Shapes.GetShapeIncludingChild("RectangleChild");

if (shapeContainerChild == null)
    throw new Exception();
    
// Save visio diagram
diagram.Save(dataDir + "GroupShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


