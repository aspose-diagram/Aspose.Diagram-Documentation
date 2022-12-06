---
title: 设置方向并控制隐藏 Visio 保存页面的导出
type: docs
weight: 20
url: /zh/net/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
description: 本节介绍如何使用 Aspose.Diagram 设置页面布局。
---
## **将 Visio 页面布局更改为纵向或横向**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)API 允许开发人员以编程方式设置 Visio 绘图页的方向。此帮助主题说明了如何完成此任务。

 Aspose.Diagram for .NET API 有[页](http://www.aspose.com/api/net/diagram/aspose.diagram/page)表示 Visio 绘图页的类。 Page 类公开的 PageSheet 属性也公开打印属性。打印属性的 PrintPageOrientation 字段允许旋转页面。它提供纵向、横向和与打印机相同的三个选项。可以使用 Aspose.Diagram API 以编程方式设置 PrintPageOrientation 字段。

这个例子的工作原理如下：

1. 将现有的 Visio diagram 加载到 Diagram 类对象中。
1. 提取一个Visio页面
1. 将其方向设置为纵向、横向或与打印机相同。
1. 保存 Visio diagram。
### **设置方向编程示例**
下面的代码示例显示了如何设置 Visio 页面的方向。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-SetVisioPageOrientation-SetVisioPageOrientation.cs" >}}
## **控制导出隐藏的 Visio 页面保存**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)API 允许开发人员在将 diagram 保存为 PDF、HTML、图像（PNG、JPEG、GIF）、SVG 和 XPS 文件时包含或排除隐藏的 Visio 页面。甚至他们可能会使用 Aspose.Diagram API 隐藏 Visio 页面，因为它的选项已经通过页面 ShapeSheet 中的单元格 UIVisibility 可用。
### **在 Visio Diagram 隐藏一个页面并设置导出选项**
 Aspose.Diagram for .NET API 有[页](http://www.aspose.com/api/net/diagram/aspose.diagram/page)表示 Visio 绘图页的类。 Page 类公开的 PageSheet 属性也公开了页面属性。页面属性的 UIVisibility 字段允许隐藏页面。然后，开发人员可以使用添加到 SVGSaveOptions、XPSSaveOptions、ImageSaveOptions、HTMLSaveOptions 和 PdfSaveOptions 类中的 ExportHiddenPage 属性。
#### **设置 PDF 的导出选项**
下面的代码显示了如何在将 diagram 保存为 PDF 格式之前设置保存选项。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToPDF-ExportOfHiddenVisioPagesToPDF.cs" >}}
#### **设置 HTML 的导出选项**
下面的代码显示了如何在将 diagram 保存为 HTML 格式之前设置保存选项。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToHTML-ExportOfHiddenVisioPagesToHTML.cs" >}}
#### **设置图像的导出选项**
下面的代码显示了如何在将 diagram 保存为图像格式之前设置保存选项。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToImage-ExportOfHiddenVisioPagesToImage.cs" >}}
#### **设置 SVG 的导出选项**
下面的代码显示了如何在将 diagram 保存为 SVG 格式之前设置保存选项。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToSVG-ExportOfHiddenVisioPagesToSVG.cs" >}}
#### **设置 XPS 的导出选项**
下面的代码显示了如何在将 diagram 保存为 XPS 格式之前设置保存选项。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToXPS-ExportOfHiddenVisioPagesToXPS.cs" >}}
