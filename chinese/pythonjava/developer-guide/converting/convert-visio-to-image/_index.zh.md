---
title: 将 Visio 转换为图像格式
linktitle: 将 Visio 转换为图像
type: docs
weight: 20
url: /zh/python-java/convert-visio-to-image/
description: This topic show you how to convert Visio to various images formats using Aspose.Diagram for Python via Java. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to PNG, JPEG, BMP images with a几行代码。
---
## **将图表导出为图像文件格式**
本文介绍如何通过 Java 将 Microsoft Visio diagram 导出为使用 Aspose.Diagram for Python 的图像。

使用 Diagram 类的构造函数读取 diagram 文件，并使用 Save 方法将 diagram 导出为任何支持的图像格式。下图显示了一个即将保存为 PNG 格式的 VSD 文件。您也可以使用其他 diagram 格式（VSS、VSSX、VSSM、VDX、VST、VSTX、VSTM、VDX、VTX 或 VSX）。

**[示例 VSD 文件。](ExportToImage.vsd)**

要将 diagram 导出到图像：

- 创建 Diagram 类的实例。
- 调用 Diagram 类的 Save 方法并设置要导出的图像格式。输出的图像文件看起来像原始文件。

**输出PNG文件。**

![待办事项：图片_替代_文本](ExportToImage.png)
### **导出到图像文件编程示例**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToImage.py" >}}

也可以将特定页面保存为图像，而不是整个文档：

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportPageToImage.py" >}}