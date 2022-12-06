---
title: 将 Visio 转换为图像格式
linktitle: 将 Visio 转换为图像
type: docs
weight: 20
url: /zh/python-net/convert-visio-to-image/
description: 本主题向您展示如何将 Aspose.Diagram 允许将 Visio 转换为各种图像格式。使用几行代码将 Visio、VSD、VSS、VDW、VST、VSDX、VSSX、VSTX、VSDM、VSTM、VSSM 转换为 PNG、JPEG、BMP 图像。
---
## **将图表导出为图像文件格式**
本文介绍了如何使用 将 Microsoft Visio diagram 导出到图像[Aspose.Diagram for .NET](https://products.aspose.com/diagram/python-net/)API。使用 [Diagram] 类构造函数读取 diagram 文件，并使用 Save 方法将 diagram 导出为任何支持的图像格式。

要将 diagram 导出到图像：

- 创建 Diagram 类的实例。
- 调用 Diagram 类的 Save 方法并设置要导出的图像格式。输出的图像文件看起来像原始文件。
### **导出 Microsoft Visio 绘图到图像文件**
{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToImage.py" >}}

也可以将特定页面保存为图像，而不是整个文档：

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportPageToImage.py" >}}