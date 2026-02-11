---
title: 连接形状
type: docs
weight: 90
url: /zh/net/connect-shapes/
description: 本节介绍如何使用 Aspose.Diagram 连接两个形状。
---
## **连接形状**
本节介绍如何使用 Aspose.Diagram for .NET 连接两个形状。
### **连接形状**
这[通过连接器连接形状](https://reference.aspose.com/diagram/net/aspose.diagram.page/connectshapesviaconnector/methods/1) method connect two shapes via a connector in the [页](http://www.aspose.com/api/net/diagram/aspose.diagram/page)班级。

下面的代码显示了如何：

1. 从模板创建一个 diagram。
1. 向页面添加两个矩形形状。
1. 向页面添加连接器形状。
1. 使用 ConnectShapesViaConnector 方法将两个矩形与连接器连接起来
1. 保存 diagram
#### **连接形状编程示例**
在您的 .NET 应用程序中使用以下代码连接使用 Aspose.Diagram for .NET 的形状。


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


|**结果**|
|:- |
|![ConnectShapes_out.vsdx](ConnectShapes.png)|
