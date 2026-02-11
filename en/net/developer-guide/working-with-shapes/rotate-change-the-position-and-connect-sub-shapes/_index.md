---
title: Rotate, Change the Position and Connect Sub-Shapes
type: docs
weight: 30
url: /net/rotate-change-the-position-and-connect-sub-shapes/
description: This section explains how to rotate a visio shape with Aspose.Diagram.
---

## **Rotate a Shape with Suitable Angle**
Aspose.Diagram for .NET allows you to rotate a shape to any angle. The SetAngle method exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class can be used to rotate a shape to any desired angle. It takes a single parameter as an angle.
### **Rotate a Shape Programming Sample**
Use the following code in your .NET application to rotate a shape using Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");
// Get shape by id
Shape shape = page.Shapes.GetShape(16);

// Add a shape and set the angle
shape.SetAngle(190);

// Save diagram
diagram.Save(dataDir + "RotateVisioShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Change the Position of a Shape**
The [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Class allows you to change the position of a shape. The connector line automatically adjusts when the shape is moved to a different position. The Move and MoveTo methods, exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, support changing the position of a shape as a part of a group or not. The code examples in this article move a shape on the page.

The process for moving a shape is:

1. Load a diagram.
1. Find a particular shape.
1. Move shape to a different location
1. Save the diagram.
### **Change Position Programming Sample**
The code snippet below shows how to move the shape. The code retrieves a Visio page by name and shape by ID 16, and moves its position.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");
// Get shape by id
Shape shape = page.Shapes.GetShape(16);
// Move shape from its position, it adds values in coordinates
shape.Move(1, 1);

// Save diagram
diagram.Save(dataDir + "MoveVisioShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Connect Sub-shapes of the Groups**
This topic elaborates how to connect two sub-shapes of two different group shapes in Microsoft Visio diagrams using Aspose.Diagram for .NET. The ConnectShapesViaConnector method exposed by the [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class can be used to connect the shapes by their IDs. The AddShape method, exposed by the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class, can be used to add a shape.

The code below shows how to:

1. Load a sample file.
1. Access a particular page.
1. Add dynamic connector shape to the selected page.
1. Connect sub-shapes
### **Connect Sub-shapes Programming Sample**
Use the following code in your .NET application to connect the sub-shapes of two different group shapes using Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Set sub shape ids
long shapeFromId = 2;
long shapeToId = 4;

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Access a particular page
Page page = diagram.Pages.GetPage("Page-3");
           
// Initialize connector shape
Shape shape = new Shape();
shape.Line.EndArrow.Value = 4;
shape.Line.LineWeight.Value = 0.01388;

// Add shape
long connecter1Id = diagram.AddShape(shape, "Dynamic connector", page.ID);
// Connect sub-shapes
page.ConnectShapesViaConnector(shapeFromId, ConnectionPointPlace.Right, shapeToId, ConnectionPointPlace.Left, connecter1Id);
// Save Visio drawing
diagram.Save(dataDir + "ConnectVisioSubShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Get the Shapes Connected to a Particular Shape**
[Add and Connect Visio Shapes](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) explains how to add a shape and connect it to other shapes in Microsoft Visio diagrams using Aspose.Diagram for .NET. It is also possible to find shapes that are connected to a specific shape.

The ConnectedShapes method exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class can be used to get the IDs of the shapes connected to a shape. The GetShape method, exposed by the [ShapeCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) class, can then be used to find a shape by its ID.

The code below shows how to:

1. Load a sample file.
1. Access a particular shape.
1. Get the names of all of the shapes connected to the selected shape.
### **Get Shapes Programming Sample**
Use the following code in your .NET application to find all the shapes connected to a specific shape using Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get shape by id
Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(16);
// Get connected shapes
long[] connectedShapeIds = shape.ConnectedShapes(ConnectedShapesFlags.ConnectedShapesAllNodes, null);

foreach (long id in connectedShapeIds)
{
    shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(id);
    Console.WriteLine("ID: " + shape.ID + "\t\t Name: " + shape.Name);
}

{{< /highlight >}}

