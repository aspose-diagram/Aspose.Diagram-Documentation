---
title: 使用连接器类型形状
type: docs
weight: 70
url: /zh/net/working-with-connector-type-shape/
description: 本节介绍如何使用 Aspose.Diagram 设置连接器外观。
---
## **在 Visio 中设置连接器类型形状的外观**
本主题详细说明开发人员如何使用 Aspose.Diagram for .NET 更改动态连接器类型形状的外观。
### **设置连接器外观**
公开的 SetConnectorsType 方法[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类可用于设置连接器类型形状的外观。

下面的代码显示了如何：

1. 加载示例 diagram。
1. 获取特定页面。
1. 获得特定的连接器形状。
1. 设置形状的外观。
1. 保存 diagram
#### **设置连接器外观编程样例**
在您的 .NET 应用程序中使用以下代码，使用 Aspose.Diagram for .NET 设置连接器类型形状的外观。

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
## **选择连接器形状的重新布线选项**
ConFixedCode 属性由[布局](http://www.aspose.com/api/net/diagram/aspose.diagram/layout)类可用于选择重新路由选项。 Layout 属性，由[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类，会用到。

下面的代码显示了如何：

1. 加载示例文件。
1. 获取特定页面。
1. 获得特定的连接器形状。
1. 设置重新路由选项。
1. 保存 diagram。
### **选择重新路由选项编程示例**
在您的 .NET 应用程序中使用以下代码选择使用 Aspose.Diagram for .NET 的连接器形状的重新布线选项。

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
