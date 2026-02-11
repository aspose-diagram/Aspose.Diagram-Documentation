---
title: Working with Connector Type Shape
type: docs
weight: 70
url: /net/working-with-connector-type-shape/
description: This section explains how to set Connector Appearance with Aspose.Diagram.
---

## **Set Appearance of the Connector Type Shape in Visio**
This topic elaborates how developers can change the appearance of dynamic connector type shape using Aspose.Diagram for .NET.
### **Set Connector Appearance**
The SetConnectorsType method exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class can be used to set appearance of the connector type shape.

The code below shows how to:

1. Load a sample diagram.
1. get a particular page.
1. get a particular connector shape.
1. set appearance of the shape.
1. save diagram
#### **Set Connector Appearance Programming Sample**
Use the following code in your .NET application to set appearance of the connector type shape using Aspose.Diagram for .NET.

```
{{< highlight "csharp" >}}
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
```
## **Select Reroute Option of the Connector Shape**
The ConFixedCode property exposed by the [Layout](http://www.aspose.com/api/net/diagram/aspose.diagram/layout) class can be used to select reroute option. The Layout property, exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, will be used.

The code below shows how to:

1. Load a sample file.
1. get a particular page.
1. get a particular connector shape.
1. set reroute options.
1. save diagram.
### **Select Reroute Option Programming Sample**
Use the following code in your .NET application to select the rerouting option of the connector shape using Aspose.Diagram for .NET.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

// Get a particular connector shape
Shape shape = page.Shapes.GetShape(18);
// Set reroute option
shape.Layout.ConFixedCode.Value = ConFixedCodeValue.NeverReroute;

// Save Visio diagram
diagram.Save(dataDir + "RerouteConnectors_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
