---
title: Convert Visio to PDF format 
linktitle: Convert Visio to PDF
type: docs
weight: 10
url: /zh/python-net/convert-visio-to-pdf/
description: This topic show you how to Aspose.Diagram allows to convert Visio to PDF formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PDF with a few lines of code.
---
## **Export to PDF**
{{% alert color="primary" %}}

Aspose.Diagram for Python via .NET directly writes the information about the API and Version Number in output documents. For example, upon rendering a Drawing to PDF, Aspose.Diagram for .NET populates **应用**值为“Aspose.Diagram”的字段和**PDF Producer**具有值的字段，例如“Aspose.Diagram 17.9”。

请注意，您不能指示 Aspose.Diagram for .NET API 更改或从输出文档中删除此信息。

{{% /alert %}}

This article explains how to export a Microsoft Visio diagram to PDF using [Aspose.Diagram for Python via .NET](https://products.aspose.com/diagram/python-net/) API.

使用 [Diagram] 类构造函数读取 diagram 文件，并使用 Save 方法将 diagram 导出为任何支持的图像格式。

The image below shows the VSD diagram that the code snippets below export PDF. You can use other diagram formats (VSS, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

|**源文件。**|
|:- |
|![待办事项：图片_替代_文本](how-to-convert-a-visio-diagram_1.png)|


To export VSD diagram to PDF:

1. 创建 Diagram 类的实例。
1. Call the Diagram classs Save method and set the output format to PDF.

Below is an image of the output PDF file.

|**输出PDF文件。**|
|:- |
|![待办事项：图片_替代_文本](how-to-convert-a-visio-diagram_2.png)|
### **Export Microsoft Visio Drawing to PDF**
The code samples show how to export Microsoft Visio Drawing to PDF using Python.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToPdf.py" >}}
