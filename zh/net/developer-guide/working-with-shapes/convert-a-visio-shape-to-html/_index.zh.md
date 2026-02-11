---
title: 将 Visio 形状转换为 Html
type: docs
weight: 10
url: /zh/net/convert-a-visio-shape-to-html/
description: 本节介绍如何使用 Aspose.Diagram 将 visio 形状转换为 html。
---
## **将 visio 形状转换为 html**
公开的 ToHTML 方法[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类可用于转换为html。

下面的代码显示了如何：

1. 加载示例 diagram。
1. 获取特定页面。
1. 得到一个特定的形状。
1. 将形状转换为 html。
### **形状到 HTML**
在您的 .net 应用程序中使用以下代码将 visio 形状转换为 html。

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToHtml.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

// Shape to HTML
Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();
shape.ToHTML("out.htm", hs);

{{< /highlight >}}
```

