---
title: 刷新形状数据
type: docs
weight: 40
url: /zh/net/refresh-shapes-data/
description: 本节介绍如何使用 Aspose.Diagram 刷新 visio 形状的形状数据。
---
## **更改形状的文本或其他形状时刷新形状的位置，包括 xform、connection 和 geom**
公开的 RefreshData 方法[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类可用于刷新形状的数据

下面的代码显示了如何：

1. 加载示例文件。
1. 访问特定形状。
1. 刷新形状的数据。
### **刷新 Shape 的数据**
在您的 .NET 应用程序中使用以下代码来刷新使用 Aspose.Diagram for .NET 的形状。


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


