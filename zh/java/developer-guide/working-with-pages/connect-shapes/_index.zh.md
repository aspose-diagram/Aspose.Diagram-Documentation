---
title: 连接形状
type: docs
weight: 90
url: /zh/java/connect-shapes/
description: 本节介绍如何用 Aspose.Diagram for Java 连接两个形状。
---
## **连接形状**
本节介绍如何使用 Aspose.Diagram for Java 连接两个形状。
### **连接形状**
这[connectShapesVia连接器](https://reference.aspose.com/diagram/java/com.aspose.diagram/page#connectShapesViaConnector(long,%20int,%20long,%20int,%20long)) method connect two shapes via a connector in the [页](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page)班级。

下面的代码显示了如何：

1. 从模板创建一个 diagram。
1. 向页面添加两个矩形形状。
1. 向页面添加连接器形状。
1. 使用 connectShapesViaConnector 方法将两个矩形与连接器连接起来
1. 保存 diagram
#### **连接形状编程示例**
使用以下代码使用 Aspose.Diagram for Java 连接形状。


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ConnectShapes.class);
String stencil = dataDir + "Basic Shapes.vss";

// create a diagram from stencil
Diagram diagram = new Diagram(stencil);
String connectorMaster = "Dynamic connector";
String rectangleMaster = "Rectangle";
// add two rectangles to page 0
long rectangle1 = diagram.addShape(2, 2, rectangleMaster, 0);
long rectangle2 = diagram.addShape(2, 4, rectangleMaster, 0);
// add a connector to page 0
Shape connector1 = new Shape();
long connecter1Id = diagram.addShape(connector1, connectorMaster, 0);
// connect the two rectangles with the connector
diagram.getPages().get(0).connectShapesViaConnector(rectangle1, ConnectionPointPlace.RIGHT, rectangle2, ConnectionPointPlace.BOTTOM, connecter1Id);

// If the connection of shapes has name, we also could use connection name to connect like below
//diagram.getPages().get(0).connectShapesViaConnector(shape1, "Port7", shape2, "Port21", connecter1Id);
// The code line above is equal to the below two lines
//diagram.getPages().get(0).glueShapeToConnectorBeginX(shape1, "Port7", connecter1Id);
//diagram.getPages().get(0).glueShapeToConnectorEndX(shape2, "Port21", connecter1Id);

// Save diagram
diagram.save(dataDir + "ConnectShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


|**结果**|
|:- |
|![ConnectShapes_out.vsdx](ConnectShapes.png)|
