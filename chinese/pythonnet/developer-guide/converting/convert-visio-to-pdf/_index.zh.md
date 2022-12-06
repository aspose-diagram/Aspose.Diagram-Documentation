---
title: 将Visio转换为PDF格式
linktitle: 将 Visio 转换为 PDF
type: docs
weight: 10
url: /zh/python-net/convert-visio-to-pdf/
description: 本主题向您展示如何将 Aspose.Diagram 允许将 Visio 转换为 PDF 格式。使用几行代码将 VSD、VSS、VDW、VST、VSDX、VSSX、VSTX、VSDM、VSTM、VSSM 转换为 PDF。
---
## **导出为 PDF**
{{% alert color="primary" %}}

Aspose.Diagram for Python via .NET 直接在输出文件中写入API和版本号的信息。例如，在将绘图渲染为 PDF 时，Aspose.Diagram for .NET 会填充**应用**值为“Aspose.Diagram”的字段和**PDF制作器**具有值的字段，例如“Aspose.Diagram 17.9”。

请注意，您不能指示 Aspose.Diagram for .NET API 更改或从输出文档中删除此信息。

{{% /alert %}}

本文介绍如何使用 将 Microsoft Visio diagram 导出为 PDF[Aspose.Diagram 为 Python 通过 .NET](https://products.aspose.com/diagram/python-net/) API.

使用 [Diagram] 类构造函数读取 diagram 文件，并使用 Save 方法将 diagram 导出为任何支持的图像格式。

下图显示了下面的代码片段导出 PDF 的 VSD diagram。您也可以使用其他 diagram 格式（VSS、VSSM、VDX、VST、VSTX、VDX、VTX 或 VSX）。

|**源文件。**|
|:- |
|![待办事项：图片_替代_文本](how-to-convert-a-visio-diagram_1.png)|


要将 VSD diagram 导出为 PDF：

1. 创建 Diagram 类的实例。
1. 调用Diagram类的Save方法，设置输出格式为PDF。

下面是输出 PDF 文件的图像。

|**输出 PDF 文件。**|
|:- |
|![待办事项：图片_替代_文本](how-to-convert-a-visio-diagram_2.png)|
### **将 Microsoft Visio 图纸导出为 PDF**
代码示例显示了如何使用 Python 将 Microsoft Visio 绘图导出为 PDF。

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToPdf.py" >}}
