---
title: 将Visio转换为PDF格式
linktitle: 将 Visio 转换为 PDF
type: docs
weight: 10
url: /zh/python-java/convert-visio-to-pdf/
description: This topic show you how to convert Visio to PDF formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to PDF with a few lines of code.
---
## **导出为 PDF**
{{% alert color="primary" %}}

Aspose.Diagram for Python via Java 直接在输出文件中写入API和版本号的信息。例如，在将绘图渲染为 PDF 时，Aspose.Diagram for Java 会填充**应用**值为“Aspose.Diagram”的字段和**PDF制作器**具有值的字段，例如“Aspose.Diagram 17.9”。

请注意，您不能通过 Java 指示 Aspose.Diagram 为 Python 更改或从输出文档中删除此信息。

{{% /alert %}}

本文介绍如何使用 Aspose.Diagram for Python via Java 将 Microsoft Visio diagram 导出为 PDF。

使用 Diagram 类的构造函数读取 diagram 文件，并使用 Save 方法将 diagram 导出为任何支持的图像格式。

[VSD diagram](ExportToPDF.vsd)是导出 PDF 的示例图形文件。您也可以使用其他 diagram 格式（VSS、VSSX、VSSM、VDX、VST、VSTX、VSTM、VDX、VTX 或 VSX）。

要将 VSD diagram 导出为 PDF：

1. 创建 Diagram 类的实例。
1. 调用Diagram类的Save方法，设置输出格式为PDF。

### **导出为 PDF 编程示例**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToPDF.py" >}}

### **拆分多个页面**
Aspose.Diagram for Java 允许拆分多个页面，同时将 Microsoft Visio Diagram 转换为 PDF。以下代码片段显示了该功能。

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.py" >}}
