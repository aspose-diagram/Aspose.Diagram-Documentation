---
title: 设置方向并控制隐藏 Visio 保存页面的导出
type: docs
weight: 20
url: /zh/java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
---
## **将 Visio 页面布局更改为纵向或横向**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API 允许开发人员以编程方式设置 Visio 绘图页的方向。此帮助主题说明了如何完成此任务。

 Aspose.Diagram for Java API 有[页](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page)表示 Visio 绘图页的类。 Page 类公开的 PageSheet 属性也公开打印属性。打印属性的 PrintPageOrientation 字段允许旋转页面。它提供纵向、横向和与打印机相同的三个选项。可以使用 Aspose.Diagram API 以编程方式设置 PrintPageOrientation 字段。

这个例子的工作原理如下：

1. 将现有的 Visio diagram 加载到 Diagram 类对象中。
1. 提取一个Visio页面
1. 将其方向设置为纵向、横向或与打印机相同。
1. 保存 Visio diagram。
### **设置方向编程示例**
下面的代码示例显示了如何设置 Visio 页面的方向。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-SetVisioPageOrientation-SetVisioPageOrientation.java" >}}
## **控制导出隐藏的 Visio 页面保存**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API allows developers to include or exclude hidden Visio pages on saving diagram to PDF, HTML, Image (PNG, JPEG, GIF), SVG, and XPS files. Even they may hide Visio pages using Aspose.Diagram API because its option is already available through the cell UIVisibility in the page ShapeSheet.
### **在 Visio Diagram 隐藏一个页面并设置导出选项**
 Aspose.Diagram for Java API 有[页](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page)表示 Visio 绘图页的类。 Page 类公开的 PageSheet 属性也公开了页面属性。页面属性的 UIVisibility 字段允许隐藏页面。然后，开发人员可以使用添加到 SVGSaveOptions、XPSSaveOptions、ImageSaveOptions、HTMLSaveOptions 和 PdfSaveOptions 类中的 ExportHiddenPage 属性。
#### **Set the Export Option for PDF**
The code below shows how to set save options before saving a diagram to PDF format.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExporToHiddenVisioPagesToPdf-ExporToHiddenVisioPagesToPdf.java" >}}
#### **Set the Export Option for HTML**
The code below shows how to set save options before saving a diagram to HTML format.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExportOfHiddenVisioPagesToHtml-ExportOfHiddenVisioPagesToHtml.java" >}}
#### **设置图像的导出选项**
下面的代码显示了如何在将 diagram 保存为图像格式之前设置保存选项。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExportOfHiddenVisioPagesToImage-ExportOfHiddenVisioPagesToImage.java" >}}
#### **Set the Export Option for SVG**
The code below shows how to set save options before saving a diagram to SVG format.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExportOfHiddenVisioPagesToSVG-ExportOfHiddenVisioPagesToSVG.java" >}}
