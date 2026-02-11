---
title: Add Connection Point To Shape
type: docs
weight: 70
url: /net/add-connection-point-to-shape/
description: This section explains how to add connection point to a visio shape with Aspose.Diagram.
---

## **Add Connection Point To a Shape in Visio**
This topic elaborates how developers can add connection point to a visio shape using Aspose.Diagram for .NET.
### **Add Connection Point**
The [Connections](https://reference.aspose.com/diagram/net/aspose.diagram/shape/properties/connections) object represents the connection collection in the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class.

The code below shows how to:

1. Load a sample diagram.
1. get a particular page.
1. get a particular shape.
1. new a connection
1. set the property of connection 
1. add connection to shape
1. save diagram
#### **Add connection point to shape Programming Sample**
Use the following code in your .NET application to add connection to a shape using Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");

// Get a particular page
Page page = diagram.Pages.GetPage("Page-3");
// Get a dynamic connector type shape by id
Shape shape = page.Shapes.GetShape(18);
// Set dynamic connector appearance
shape.SetConnectorsType(ConnectorsTypeValue.StraightLines);

// Saving Visio diagram
diagram.Save(dataDir + "SetConnectorAppearance_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

