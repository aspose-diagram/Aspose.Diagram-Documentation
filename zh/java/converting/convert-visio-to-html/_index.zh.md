﻿---
title: Convert Visio to HTML format 
linktitle: Convert Visio to HTML
type: docs
weight: 30
url: /zh/java/convert-visio-to-html/
description: This topic show you how to Aspose.Diagram allows to convert Visio to html formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to html with a few lines of code.
---
## **导出 Visio 到 HTML** **导出 Visio 到 HTML**
This article explains how to export a Microsoft Visio diagram to HTML using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

使用[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class constructor to read the diagram files and the Save method to export the diagram to any supported image format. Developers can save resultant HTML in the local storage or directly to a stream instance.

1. [Save resultant HTML in the local storage](/diagram/zh/java/how-to-convert-a-visio-diagram/).
1. [Save resultant HTML in a stream instance](/diagram/zh/java/how-to-convert-a-visio-diagram/).

The image below shows a VSD file about to be saved to PNG format. You can use other diagram formats (VSDX, VSTM, VSTM, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

**输入 diagram。**

![待办事项：图片_替代_文本](http://i.imgur.com/YX4BNNq.png)

In order to export VSD diagram to HTML, perform the following steps:

1. 创建 Diagram 类的实例。
1. Call the Dagram class' Save method and set HTML as the output format.

下图显示了输出 HTML 文件。

**Output HTML diagram.**

![待办事项：图片_替代_文本](http://i.imgur.com/syavUqI.png)
### **Save resultant HTML in the local storage**
生成的文件可以通过传递完整的路径字符串来保存，包括文件名和扩展名，例如@"c:\temp\MyOutput.html"。
#### **Save Resultant HTML in Local Storage Programming Sample**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToHTML-ExportToHTML.java" >}}



### **Save resultant HTML in a stream instance**
It is for use case to save the resultant HTML in a database or repository without storing it in the local storage. This feature also embeds other resultant resources of the HTML, e.g. fonts, CSS (containing the style information) and images. Since it saves a single HTML file into the stream instance.
#### **Save Resultant HTML in a Stream Programming Sample**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportHTMLinStream-ExportHTMLinStream.java" >}}
