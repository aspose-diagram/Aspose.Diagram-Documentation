﻿---
title: 将 Visio 转换为图像格式
linktitle: 将 Visio 转换为图像
type: docs
weight: 20
url: /zh/java/convert-visio-to-image/
description: This topic show you how to Aspose.Diagram allows to convert Visio to various images formats. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PNG, JPEG, BMP images with a few lines of code.
---
## **将图表导出为图像文件格式**
本文介绍了如何使用 将 Microsoft Visio diagram 导出到图像[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

使用[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class' constructor to read the diagram files and the Save method to export the diagram to any supported image format.The image below shows a VSD file about to be saved to PNG format. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.
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