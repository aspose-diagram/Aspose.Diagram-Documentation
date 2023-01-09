---
title: Visio加水印
type: docs
weight: 10
url: /zh/net/add-watermark-to-visio/
keywords: watermark, visi
description: 如何使用 .NET Diagram API 为 visio 添加水印。
---
## **创建一个 Diagram**
 Aspose.Diagram for .NET 允许您从自己的应用程序中读取和创建 Microsoft Visio 图表，无需 Microsoft Office 自动化。创建新文档的第一步是创建一个 diagram。然后[添加形状和连接器](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/)构建 diagram。使用默认构造函数[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)类创建一个新的 diagram。
### **编程范例**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-CreateDiagram-CreateDiagram.cs" >}}

这个例子的工作原理如下：

1. 创建 Diagram 类的对象。
1. 页面中visio加水印
1. 调用 Diagram 类对象的 Save 方法，并传递完整的文件路径和 DiagramSaveOptions 对象。
### **添加水印编程示例**
下面的示例代码展示了如何在 Visio diagram 中添加水印。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-AddWatermarkToVisio-AddWatermarkToVisio.cs" >}}
