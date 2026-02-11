---
title: 将 Visio 形状转换为图像
type: docs
weight: 10
url: /zh/net/convert-a-visio-shape-to-image/
description: 本节介绍如何将 visio 形状转换为具有 Aspose.Diagram 的图像。
---
## **将 visio 形状转换为图像**
本主题详细说明开发人员如何使用 Aspose.Diagram 将 visio 形状转换为图像。
公开的 ToImage 方法[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类可用于转换为图像。


下面的代码显示了如何：

1. 加载示例 diagram。
1. 获取特定页面。
1. 得到一个特定的形状。
1. 将形状转换为图像。
#### **形状到图像编程示例**
在 .net 应用程序中使用以下代码将 visio 形状转换为图像。


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToImage.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

// Shape to Image
Aspose.Diagram.Saving.ImageSaveOptions o = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);
shape.ToImage("out.png", o);

{{< /highlight >}}

