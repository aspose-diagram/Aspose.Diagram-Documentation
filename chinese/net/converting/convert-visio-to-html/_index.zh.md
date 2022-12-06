---
title: 将 Visio 转换为 HTML 格式
linktitle: 将 Visio 转换为 HTML
type: docs
weight: 30
url: /zh/net/convert-visio-to-html/
description: 本主题向您展示如何将 Aspose.Diagram 允许将 Visio 转换为 html 格式。使用几行代码将 VSD、VSS、VDW、VST、VSDX、VSSX、VSTX、VSDM、VSTM、VSSM 转换为 html。
---
## **将 Visio 导出为 HTML**
本文介绍了如何使用 将 Microsoft Visio diagram 导出到 HTML[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

使用[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)类构造函数读取 diagram 文件和 Save 方法将 diagram 导出为任何支持的图像格式。开发人员可以将生成的 HTML 保存在本地存储中或直接保存到流实例中。

1. [将生成的 HTML 保存在本地存储中](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-the-local-storage).
1. [将生成的 HTML 保存在流实例中](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-a-stream-instance).

下图显示了一个即将保存为 PNG 格式的 VSD 文件。您可以使用其他 diagram 格式（VSDX、VSDM、VSTX、VSSX、VSS、VSSM、VDX、VST、VSTX、VDX、VTX1 或 3.761）

|**输入 diagram。**|
|:- |
|![待办事项：图片_替代_文本](how-to-convert-a-visio-diagram_6.png)|
为了将 VSD diagram 导出为 HTML，请执行以下步骤：

1. 创建 Diagram 类的实例。
1. 调用 Dagram 类的 Save 方法并将 HTML 设置为输出格式。
### **将生成的 HTML 保存在本地存储中**
生成的文件可以通过传递完整的路径字符串来保存，包括文件名和扩展名，例如@"c:\temp\MyOutput.html"。
#### **将生成的 HTML 保存在本地存储编程示例中**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-ExportToHTML-ExportToHTML.cs" >}}



### **将生成的 HTML 保存在流实例中**
它适用于将生成的 HTML 保存在数据库或存储库中而不将其存储在本地存储中的用例。此功能还嵌入了 HTML 的其他结果资源，例如字体、CSS（包含样式信息）和图像。因为它将单个 HTML 文件保存到流实例中。
#### **将生成的 HTML 保存在流编程示例中**
{{< highlight "java" >}}

 // Load an existing visio diagram

Diagram diagram = new Diagram("Basic Flowchart.vsd");

// Save resultant HTML directly to a stream

MemoryStream stream = new MemoryStream();

diagram.Save(stream, SaveFileFormat.HTML);



{{< /highlight >}}
