---
title: 以编程方式保存 Visio 文档
linktitle: 保存 Visio 文件
type: docs
weight: 30
url: /zh/java/save-visio-document/
description: 本页介绍如何将 Visio 文档保存到文件，使用 Aspose.Diagram 库进行流式传输。
---
## **Visio 图纸保存概述**
使用[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\) 方法保存 Microsoft Visio 图。有允许将绘图保存到文件的重载。绘图可以保存为 Aspose.Diagram 支持的任何保存格式。有关所有支持的保存格式的列表，请参阅[保存文件格式](https://reference.aspose.com/diagram/java/com.aspose.diagram/SaveFileFormat)枚举。
## **储蓄 Visio Diagram**
 Aspose.Diagram API 的 Diagram 类表示一个 Visio 绘图，开发人员可以将其 Visio diagram 对象保存为任何支持的文件格式。要保存 Microsoft Visio 文件，只需使用[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\)方法，它接受具有完整路径的文件名或文件流对象。 Aspose.Diagram API 从文件扩展名推断保存格式，还提供一个额外的 SaveFileFormat 参数来指定输出文件格式。
### **以任何支持的文件格式保存 Visio Diagram**
使用 Aspose.Diagram API，开发人员可以将 Visio diagram 保存为任何支持的文件格式，如下所列：
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF and XAML, SVG**
### **保存 Diagram 编程示例**
下面的示例将文档保存到文件中。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-SaveVisioDiagram-SaveVisioDiagram.java" >}}
## **指定 Visio 保存选项**
有几个[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\)接受 SaveOptions 对象的方法重载。这应该是从 SaveOptions 类派生的类的对象。每个保存格式都有一个相应的类，其中包含该保存格式的保存选项，例如，SaveFileFormat.PDF 保存格式有 PdfSaveOptions。
### **Visio Diagram 保存选项**
这些示例展示了如何：

- [使用 Diagram 保存选项](/diagram/zh/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [使用 PDF 保存选项](/diagram/zh/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [使用 HTML 保存选项](/diagram/zh/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [使用图像保存选项](/diagram/zh/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [使用 SVG 保存选项](/diagram/zh/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
#### **使用 Diagram 保存选项**
下面的代码显示了如何在将文档保存为 Visio 格式之前设置保存选项。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseDiagramSaveOptions-UseDiagramSaveOptions.java" >}}



#### **使用 PDF 保存选项**
下面的代码显示了如何在将文档保存为 PDF 格式之前设置保存选项。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-UsePDFSaveOptions.java" >}}



#### **使用 HTML 保存选项**
下面的代码显示了如何在将文档保存为 HTML 格式之前设置保存选项。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseHTMLSaveOptions-UseHTMLSaveOptions.java" >}}



#### **使用图像保存选项**
下面的代码显示了如何在将文档保存为图像格式之前设置保存选项。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseImageSaveOptions-UseImageSaveOptions.java" >}}
#### **使用 SVG 保存选项**
下面的代码显示了如何在将文档保存为 SVG 格式之前设置保存选项。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseSVGSaveOptions-UseSVGSaveOptions.java" >}}
