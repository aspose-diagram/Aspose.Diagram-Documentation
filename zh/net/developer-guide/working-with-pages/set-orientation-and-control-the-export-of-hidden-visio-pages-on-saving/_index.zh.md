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

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");
// Page orientation
page.PageSheet.PrintProps.PrintPageOrientation.Value = PrintPageOrientationValue.Landscape;
// Save Visio
diagram.Save(dataDir + "SetPageOrientation_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **控制导出隐藏的 Visio 页面保存**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API allows developers to include or exclude hidden Visio pages on saving diagram to PDF, HTML, Image (PNG, JPEG, GIF), SVG, and XPS files. Even they may hide Visio pages using Aspose.Diagram API because its option is already available through the cell UIVisibility in the page ShapeSheet.
### **在 Visio Diagram 隐藏一个页面并设置导出选项**
 Aspose.Diagram for .NET API 有[页](http://www.aspose.com/api/net/diagram/aspose.diagram/page)表示 Visio 绘图页的类。 Page 类公开的 PageSheet 属性也公开了页面属性。页面属性的 UIVisibility 字段允许隐藏页面。然后，开发人员可以使用添加到 SVGSaveOptions、XPSSaveOptions、ImageSaveOptions、HTMLSaveOptions 和 PdfSaveOptions 类中的 ExportHiddenPage 属性。
#### **Set the Export Option for PDF**
The code below shows how to set save options before saving a diagram to PDF format.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = BOOL.True;

// Initialize PDF save options
PdfSaveOptions options = new PdfSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;

// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToPDF_out.pdf", options);

{{< /highlight >}}
```
#### **Set the Export Option for HTML**
The code below shows how to set save options before saving a diagram to HTML format.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = UIVisibilityValue.Visible;

// Initialize PDF save options
HTMLSaveOptions options = new HTMLSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;
// Set export option of comments
options.IsExportComments = false;

// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToHTML_out.html", options);

{{< /highlight >}}
```
#### **设置图像的导出选项**
下面的代码显示了如何在将 diagram 保存为图像格式之前设置保存选项。

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = UIVisibilityValue.Visible;

// Initialize PDF save options
ImageSaveOptions options = new ImageSaveOptions(SaveFileFormat.JPEG);
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;
// Set export option of comments
options.IsExportComments = false;

// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToImage_out.jpeg", options);

{{< /highlight >}}
```
#### **Set the Export Option for SVG**
The code below shows how to set save options before saving a diagram to SVG format.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = UIVisibilityValue.Visible;

// Initialize PDF save options
SVGSaveOptions options = new SVGSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;
// Set export guide shapes 
options.ExportGuideShapes = false;
// Set save format
options.SaveFormat = Aspose.Diagram.SaveFileFormat.SVG;
// Set SVG fit to view port
options.SVGFitToViewPort = true;
// Set export element as Rectangle
options.ExportElementAsRectTag = true;


// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToSVG_out.svg", options);

{{< /highlight >}}
```
#### **Set the Export Option for XPS**
The code below shows how to set save options before saving a diagram to XPS format.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = BOOL.True;

// Initialize PDF save options
XPSSaveOptions options = new XPSSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;

// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToXPS_out.xps", options);

{{< /highlight >}}
```
