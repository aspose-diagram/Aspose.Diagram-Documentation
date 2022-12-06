---
title: 将 Visio 转换为图像格式
linktitle: 将 Visio 转换为图像
type: docs
weight: 20
url: /zh/java/convert-visio-to-image/
description: 本主题向您展示如何将 Aspose.Diagram 允许将 Visio 转换为各种图像格式。使用几行代码将 Visio、VSD、VSS、VDW、VST、VSDX、VSSX、VSTX、VSDM、VSTM、VSSM 转换为 PNG、JPEG、BMP 图像。
---
## **将图表导出为图像文件格式**
本文介绍了如何使用 将 Microsoft Visio diagram 导出到图像[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

使用[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)类的构造函数读取 diagram 文件，Save 方法将 diagram 导出为任何支持的图像格式。下图显示了一个即将保存为 PNG 格式的 VSD 文件。您也可以使用其他 diagram 格式（VSS、VSSX、VSSM、VDX、VST、VSTX、VSTM、VDX、VTX 或 VSX）。
**源文件。请注意，箭头和三角形标签以粗体显示。**

![待办事项：图片_替代_文本](http://i.imgur.com/WOV36ek.png)

要将 diagram 导出到图像：

- 创建 Diagram 类的实例。
- 调用 Diagram 类的 Save 方法并设置要导出的图像格式。输出的图像文件看起来像原始文件。

**输出PNG文件。**

![待办事项：图片_替代_文本](http://i.imgur.com/WOV36ek.png)
### **导出到图像文件编程示例**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToImage-ExportToImage.java" >}}

也可以将特定页面保存为图像，而不是整个文档：

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportPageToImage-ExportPageToImage.java" >}}