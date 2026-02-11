---
title: 将连接点添加到形状
type: docs
weight: 70
url: /zh/net/add-connection-point-to-shape/
description: 本节介绍如何将连接点添加到具有 Aspose.Diagram 的 visio 形状。
---
## **将连接点添加到 Visio 中的形状**
本主题详细说明开发人员如何使用 Aspose.Diagram for .NET 将连接点添加到 visio 形状。
### **添加连接点**
这[连接](https://reference.aspose.com/diagram/net/aspose.diagram/shape/properties/connections)object 表示中的连接集合[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)班级。

下面的代码显示了如何：

1. 加载示例 diagram。
1. 获取特定页面。
1. 得到一个特定的形状。
1. 新连接
1. 设置连接属性
1. 为形状添加连接
1. 保存 diagram
#### **将连接点添加到形状编程示例**
在您的 .NET 应用程序中使用以下代码将连接添加到使用 Aspose.Diagram for .NET 的形状。


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

