---
title: Convert Visio to PDF format 
linktitle: Convert Visio to PDF
type: docs
weight: 10
url: /zh/net/convert-visio-to-pdf/
description: This topic show you how to Aspose.Diagram allows to convert Visio to PDF formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PDF with a few lines of code.
---
## **Export to PDF**
{{% alert color="primary" %}}

Aspose.Diagram for .NET directly writes the information about the API and Version Number in output documents. For example, upon rendering a Drawing to PDF, Aspose.Diagram for .NET populates **应用**值为“Aspose.Diagram”的字段和**PDF Producer**具有值的字段，例如“Aspose.Diagram 17.9”。

请注意，您不能指示 Aspose.Diagram for .NET API 更改或从输出文档中删除此信息。

{{% /alert %}}

This article explains how to export a Microsoft Visio diagram to PDF using [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

使用[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)类构造函数读取 diagram 文件和 Save 方法将 diagram 导出为任何支持的图像格式。

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
The code samples show how to export Microsoft Visio Drawing to PDF using C#.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-ExportToPDF-ExportToPDF.cs" >}}
### **拆分多个页面**
Aspose.Diagram for .NET allows splitting multiple pages while converting the Microsoft Visio Diagram to PDF. The following code snippet shows the functionality.  

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.cs" >}}
### **使用页面保存回调**
In case you have multiple pages, Aspose.Diagram for .NET allows using page saving callback while converting the Microsoft Visio Diagram to PDF. The following code snippet shows the functionality.  

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-PageSavingCallback.cs" >}}
#### **TestDiagramPageSavingCallback 类**
{{< highlight "java" >}}

公共类 TestDiagramPageSavingCallback ：Aspose.Diagram.Saving.IPageSavingCallback

{  public void PageStartSaving(Aspose.Diagram.Saving.PageStartSavingArgs args)  {  Console.WriteLine("开始保存 diagram 页 {0} of pages {1}", args.PageIndexs + PageIndexs + Paged_0, ar  }  public void PageEndSaving(Aspose.Diagram.Saving.PageEndSavingArgs args)  {  Console.WriteLine("结束保存 diagram 页 {0} of pages {1}", In arg +Page.Page.Page   //don't output pages after page index 8.  if (args.PageIndex >= 8)  {  args.HasMorePages = false;  }  }  }
