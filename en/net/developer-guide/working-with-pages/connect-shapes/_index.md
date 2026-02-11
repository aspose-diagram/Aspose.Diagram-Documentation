---
title: Connect Shapes
type: docs
weight: 90
url: /net/connect-shapes/
description: This section explains how to connect two shapes with Aspose.Diagram.
---

## **Connect Shapes**
This section explains how to connect two shapes using Aspose.Diagram for .NET.
### **Connect Shapes**
The [ConnectShapesViaConnector](https://reference.aspose.com/diagram/net/aspose.diagram.page/connectshapesviaconnector/methods/1) method connect two shapes via a connector in the [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class.

The code below shows how to:

1. Create a diagram from stencil.
1. Add two rectangles shape to page.
1. Add a connector shape to page.
1. Connect the two rectangles with the connector using ConnectShapesViaConnector mothod
1. save diagram
#### **Connect Shapes Programming Sample**
Use the following code in your .NET application to connect shapes using Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
string stencil = dataDir + "Basic Shapes.vss";

// create a diagram from stencil
Diagram diagram = new Diagram(stencil);
string connectorMaster = "Dynamic connector";
string rectangleMaster = "Rectangle";
// add two rectangles to page 0
long rectangle1 = diagram.AddShape(2, 2, rectangleMaster, 0);
long rectangle2 = diagram.AddShape(2, 4, rectangleMaster, 0);
// add a connector to page 0
Shape connector1 = new Shape();
long connecter1Id = diagram.AddShape(connector1, connectorMaster, 0);
// connect the two rectangles with the connector
diagram.Pages[0].ConnectShapesViaConnector(rectangle1, ConnectionPointPlace.Right, rectangle2, ConnectionPointPlace.Bottom, connecter1Id);

// If the connection of shapes has name, we also could use connection name to connect like below
//diagram.Pages[0].ConnectShapesViaConnector(shape1, "Port7", shape2, "Port21", connecter1Id);
// The code line above is equal to the below two lines
//diagram.Pages[0].GlueShapeToConnectorBeginX(shape1, "Port7", connecter1Id);
//diagram.Pages[0].GlueShapeToConnectorEndX(shape2, "Port21", connecter1Id);

// Save diagram
diagram.Save(dataDir + "ConnectShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


|**Result**|
| :- |
|![ConnectShapes_out.vsdx](ConnectShapes.png)|