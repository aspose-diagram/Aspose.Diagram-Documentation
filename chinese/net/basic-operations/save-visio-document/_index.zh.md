---
title: 以编程方式保存 Visio 文档
linktitle: 保存 Visio 文件
type: docs
weight: 30
url: /zh/net/save-visio-document/
description: 本页介绍如何将 Visio 文档保存到文件，使用 Aspose.Diagram 库进行流式传输。
---
## **Visio 图纸保存概述**
使用[Diagram.Save]()保存Microsoft Visio图纸的方法。有允许将绘图保存到文件的重载。绘图可以保存为 Aspose.Diagram 支持的任何保存格式。有关所有支持的保存格式的列表，请参阅[保存文件格式]()枚举。
## **储蓄 Visio Diagram**
 Aspose.Diagram API 的 Diagram 类表示一个 Visio 绘图，开发人员可以将其 Visio diagram 对象保存为任何支持的文件格式。要保存 Microsoft Visio 文件，只需使用[Diagram.Save]()方法，它接受具有完整路径的文件名或文件流对象。 Aspose.Diagram API 从文件扩展名推断保存格式，还提供了一个额外的 SaveFileFormat 参数来指定输出文件格式。
### **以任何支持的文件格式保存 Visio Diagram**
使用 Aspose.Diagram API，开发人员可以将 Visio diagram 保存为任何支持的文件格式，如下所列：
**VSDX、VSDM、VSSX、VSSM、VSTX、VSTM、VDX、VSX、VTX、TIFF、PNG、BMP、EMF、JPEG、PDF、XPS、GIF、HTML、SWF 和 SVG、SVG**
### **保存 Diagram 编程示例**
下面的示例将文档保存到文件中。

{{< highlight "java" >}}

 // Save a Visio diagram

diagram.Save(GetMyDir() + "MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **指定 Visio 保存选项**
有几个[Diagram.Save]()接受 SaveOptions 对象的方法重载。这应该是从 SaveOptions 类派生的类的对象。每个保存格式都有一个相应的类，其中包含该保存格式的保存选项。例如，SaveFileFormat.PDF 保存格式有 PdfSaveOptions。
### **Visio Diagram 保存选项**
这些示例展示了如何：

- [使用 Diagram 保存选项](https://docs.aspose.com/diagram/net/save-visio-document/).
- [使用 PDF 保存选项](https://docs.aspose.com/diagram/net/save-visio-document/).
- [使用 HTML 保存选项](https://docs.aspose.com/diagram/net/save-visio-document/).
- [使用图像保存选项](https://docs.aspose.com/diagram/net/save-visio-document/).
- [使用 SVG 保存选项](https://docs.aspose.com/diagram/net/save-visio-document/).
- [使用 SWF 保存选项](https://docs.aspose.com/diagram/net/save-visio-document/).
#### **使用 Diagram 保存选项**
下面的代码显示了如何在将文档保存为 Visio 格式之前设置保存选项。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseDiagramSaveOptions-UseDiagramSaveOptions.cs" >}}



#### **使用 PDF 保存选项**
下面的代码显示了如何在将文档保存为 PDF 格式之前设置保存选项。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-UsePDFSaveOptions.cs" >}}



#### **使用 HTML 保存选项**
下面的代码显示了如何在将文档保存为 HTML 文件格式之前设置保存选项。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseHTMLSaveOptions-UseHTMLSaveOptions.cs" >}}



#### **使用图像保存选项**
下面的代码显示了如何在将文档保存为图像文件格式之前设置保存选项。



{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseImageSaveOptions-UseImageSaveOptions.cs" >}}


使用 SVG 保存选项

下面的代码显示了如何在将文档保存为 SVG 格式之前设置保存选项。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseSVGSaveOptions-UseSVGSaveOptions.cs" >}}


使用 SWF 保存选项

下面的代码显示了如何在将文档保存为 SWF 格式之前设置保存选项。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseSWFSaveOptions-UseSWFSaveOptions.cs" >}}

有时，开发人员需要以编程方式将 Visio 图表保存或导出为不同的文件格式（如 VDX、PDF、JPEG 等）。
## **将 VSD 文件保存为不同的文件格式（VDX、PDF 和 JPEG）**
本文提供了一个代码示例，说明如何使用[VSTO](https://docs.aspose.com/diagram/net/save-visio-document/)和[Aspose.Diagram for .NET](https://docs.aspose.com/diagram/net)以编程方式将 Microsoft Visio VSD 文件保存为 VDX 文件、PDF 文件或 JPEG 文件。下面是 VSTO 和 Aspose.Diagram for .NET 的并行代码片段，解释了如何将 VSD 文件保存为不同的文件格式。您会注意到 Aspose.Diagram 代码更短。随意使用代码并更改它以满足您的特定需求。
### **使用 VSTO 将 VSD 文件保存为其他格式**
VSTO 允许您使用 Microsoft Visio 文件进行编程。要将文件保存为其他格式：

1. 创建一个 Visio 应用程序对象。
1. 使应用程序对象不可见。
1. 加载 diagram。
1. 保存为 VDX，PDF 和 JPEG。
1. 退出 Visio 应用程序对象。
#### **使用 VSTO 编程示例保存 VSD 文件**
{{% alert color="primary" %}} 

使用 Visio = Microsoft.Office.Interop.Visio；
进口 Visio = Microsoft.Office.Interop.Visio

{{% /alert %}} 

**例子：**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-SaveDiagramTo-VDX-PDF-JPEG-withVSTO-SaveDiagramTo_VDX_PDF_JPEG_withVSTO.cs" >}}
### ` `**用Aspose.Diagram将VSD文件保存为其他格式 for .NET**
使用Aspose.Diagram，开发者不需要在机器上使用Microsoft Office Visio，可以独立于Microsoft Office自动化工作。

下面的代码片段展示了如何：

1. 加载一个 diagram。
1. 将 diagram 保存为 VSX，PDF 和 JPEG。
#### **用 Aspose.Diagram 保存 VSD 文件 for .NET 编程示例**
{{% alert color="primary" %}} 

使用 Aspose.Diagram；
进口 Aspose.Diagram

{{% /alert %}} 

**例子：**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-SaveDiagramTo-VDX-PDF-JPEG-withAspose-SaveDiagramTo_VDX_PDF_JPEG_withAspose.cs" >}}
