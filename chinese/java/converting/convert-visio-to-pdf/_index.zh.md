---
title: Convert Visio to PDF format 
linktitle: Convert Visio to PDF
type: docs
weight: 10
url: /zh/java/convert-visio-to-pdf/
description: This topic show you how to Aspose.Diagram allows to convert Visio to PDF formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PDF with a few lines of code.
---
## **Exporting to PDF**
{{% alert color="primary" %}}

Aspose.Diagram for Java directly writes the information about the API and Version Number in output documents. For example, upon rendering a Drawing to PDF, Aspose.Diagram for Java populates **应用**值为“Aspose.Diagram”的字段和**PDF Producer**具有值的字段，例如“Aspose.Diagram 17.9”。

请注意，您不能指示 Aspose.Diagram for Java API 更改或从输出文档中删除此信息。

{{% /alert %}}

This article explains how to export a Microsoft Visio diagram to PDF using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

使用[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram)类的构造函数读取 diagram 文件和 Save 方法将 diagram 导出为任何支持的图像格式。

The image below shows the VSD diagram that the code snippets below export PDF. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

**源文件。**

![待办事项：图片_替代_文本](how-to-convert-a-visio-diagram_1.png)

To export VSD diagram to PDF:

1. 创建 Diagram 类的实例。
1. Call the Diagram classs Save method and set the output format to PDF.

Below is an image of the output PDF file.

**输出PDF文件。**

![待办事项：图片_替代_文本](how-to-convert-a-visio-diagram_2.png)
### **Exporting to PDF Programming Sample**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToPDF-ExportToPDF.java" >}}
### **拆分多个页面**
Aspose.Diagram for Java allows splitting multiple pages while converting the Microsoft Visio Diagram to PDF. The following code snippet shows the functionality.  

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.java" >}}
### **使用页面保存回调**
In case you have multiple pages, Aspose.Diagram for Java allows using page saving callback while converting the Microsoft Visio Diagram to PDF. The following code snippet shows the functionality.  

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-DiagramConversions-DocumentConversionProgress-1.java" >}}

#### **TestDiagramPageSavingCallback 类**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-DiagramConversions-DocumentConversionProgress-2.java" >}}
