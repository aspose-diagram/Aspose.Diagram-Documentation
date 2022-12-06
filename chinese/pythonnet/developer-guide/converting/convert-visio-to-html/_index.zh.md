---
title: 将 Visio 转换为 HTML 格式
linktitle: 将 Visio 转换为 HTML
type: docs
weight: 30
url: /zh/python-net/convert-visio-to-html/
description: 本主题向您展示如何将 Aspose.Diagram 允许将 Visio 转换为 html 格式。使用几行代码将 VSD、VSS、VDW、VST、VSDX、VSSX、VSTX、VSDM、VSTM、VSSM 转换为 html。
---
## **将 Visio 导出为 HTML**
本文介绍了如何使用 将 Microsoft Visio diagram 导出到 HTML[Aspose.Diagram 为 Python 通过 .NET](https://products.aspose.com/diagram/python-net/) API.

使用 Diagram 类构造函数读取 diagram 文件，并使用 Save 方法将 diagram 导出为任何支持的图像格式。开发人员可以将生成的 HTML 保存在本地存储中或直接保存到流实例中。

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
{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToHTML.py" >}}
