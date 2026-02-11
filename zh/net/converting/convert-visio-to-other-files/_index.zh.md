---
title:  Visio转其他格式
linktitle:  Visio转其他格式
type: docs
weight: 40
url: /zh/net/convert-visio-to-other-files/
description: This topic show you how to Aspose.Diagram allows to convert Visio to SVG,XPS,XML,XAML formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to SVG,XPS,XML,XAML with a few lines of code.
---
## **导出为 XML**
### **Export Microsoft Visio Drawing to PDF**
The code samples show how to export Microsoft Visio Drawing to PDF using C#.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExportToPDF.vsd");

MemoryStream pdfStream = new MemoryStream();
// Save diagram
diagram.Save(pdfStream, SaveFileFormat.PDF);

// Create a PDF file
FileStream pdfFileStream = new FileStream(dataDir + "ExportToPDF_out.pdf", FileMode.Create, FileAccess.Write);
pdfStream.WriteTo(pdfFileStream);
pdfFileStream.Close();

pdfStream.Close();

// Display Status.
System.Console.WriteLine("Conversion from vsd to pdf performed successfully.");

{{< /highlight >}}
```

本文介绍了如何使用 将 Microsoft Visio diagram 导出到 XML[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

- VDX 定义了一个 XML diagram。
- VTX 定义了一个 XML 模板。
- VSX 定义了一个 XML 模板。

这[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)类的构造函数读取 diagram，Save 方法用于以不同的文件格式保存或导出 diagram。本文中的代码片段显示了如何使用 Save 方法将 Visio 文件保存到[VDX](https://docs.aspose.com/diagram/net/save-visio-document/), [VTX](https://docs.aspose.com/diagram/net/save-visio-document/)和[VSX](https://docs.aspose.com/diagram/net/save-visio-document/).

下图显示了在下面的代码片段中导出的 diagram。导出的文件显示在每个代码片段之前。

|**A Microsoft Visio diagram 即将出口。**|
|:- |
|![待办事项：图片_替代_文本](how-to-convert-a-visio-diagram_3.png)|

### **导出 VSD 到 VDX**
VDX 是一种基于架构的 XML 文件格式，可让您以 Microsoft Visio 以外的产品可以读取的格式保存图表。这是一种在软件应用程序之间传输图表和保留可编辑数据的有用格式。

将 VSD diagram 导出到 VDX：

1. 创建 Diagram 类的实例。
1. 调用Diagram类的Save方法将Visio绘图文件写入VDX。

|**导出的 VDX 文件。**|
|:- |
|![待办事项：图片_替代_文本](how-to-convert-a-visio-diagram_4.png)|

### **出口从VSD到VSX**
VSX 是一种用于定义模板的 XML 格式，模板是构建 diagram 的基本对象。当 Visio 文件转换为 VSX 时，仅导出模板。

将 VSD diagram 导出到 VSX：

- 创建 Diagram 类的实例。
- 调用Diagram类的Save方法将Visio绘图文件写入VSX。
### **导出 VSD 到 VTX**
TVX 是模板文件的 XML 表示，并存储文档的设置。

将 VSD diagram 导出到 VTX：

1. 创建 Diagram 类的实例。
1. 调用diagram类的Save方法写入VTX格式的Visio图形文件。
### **导出 Microsoft Visio 绘图到 XML**
代码示例显示如何使用 C# 将 Microsoft Visio 绘图导出为 XML。

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
            
/* 1. Exporting VSDX to VDX */
// Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToXML.vsd");

// Save input VSD as VDX
diagram.Save(dataDir + "ExportToXML_out.vdx", SaveFileFormat.VDX);

/* 2. Exporting from VSD to VSX */
// Call the diagram constructor to load diagram from a VSD file
            
// Save input VSD as VSX
diagram.Save(dataDir + "ExportToXML_out.vsx", SaveFileFormat.VSX);
            
/* 3. Export VSD to VTX */
// Save input VSD as VTX
diagram.Save(dataDir + "ExportToXML_out.vtx", SaveFileFormat.VTX);

{{< /highlight >}}
```

## **Export to XPS**
This article explains how to export a Microsoft Visio diagram to XPS using [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.
使用[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)类的构造函数读取 diagram 文件和 Save 方法将 diagram 导出为任何支持的图像格式。

The code snippets in this article takes the diagram below as an input. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

|**源文档。**|
|:- |
|![待办事项：图片_替代_文本](how-to-convert-a-visio-diagram_5.png)|


To export VSD diagram to XPS:

1. 创建 Diagram 类的实例。
1. Call the Diagram class' Save method and set XPS as the output format.
### **Export Microsoft Visio Drawing to XPS**
The code samples show how to export Microsoft Visio Drawing to XPS using C#.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Open a VSD file
Diagram diagram = new Diagram(dataDir + "LayOutShapesInCompactTreeStyle.vdx");

// Save diagram to an XPS format
diagram.Save(dataDir + "ExportToXPS_out.xps", SaveFileFormat.XPS);

{{< /highlight >}}
```

## **Export a Diagram to SVG**
This article explains how to export a Microsoft Visio diagram to SVG (Scalable Vector Graphics) using [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

使用[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)类的构造函数读取 diagram 文件和 Save 方法将 diagram 导出为任何支持的图像格式。

To export VSD diagram to SVG, perform the following steps:

1. 创建 Diagram 类的实例。
1. Call the class' Save method and set SVG as the export format.
### **Export Microsoft Visio Drawing to SVG**
The code samples show how to export a diagram to SVG using C#.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExportToSVG.vsd");

// Save SVG Output file
diagram.Save(dataDir + "Output.svg", SaveFileFormat.SVG);

{{< /highlight >}}
```
## **Export to SWF**
This article explains how to export a Microsoft Visio diagram to SWF using [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

使用[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' constructors to read the diagram files and then the Diagram class' Save method to export the diagram to SWF format. The image below shows the input VSD file that the code renders to SWF. You can use other diagram formats (VSS, VSSX, VSSM, VDW, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

|**输入 diagram。**|
|:- |
|![待办事项：图片_替代_文本](how-to-convert-a-visio-diagram_7.png)|

在代码之后，有一个输出图像。

To export VSD diagram to SWF::

- 创建 Diagram 类的实例。
- Call the Diagram class' Save method and provide SWF format to export your diagram to SWF.
### **嵌入式查看器编程示例**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();
// Load diagram
Diagram diagram = new Diagram(dataDir + "ActvDir.vsd");
// Save diagram
diagram.Save(dataDir + "Output_out.swf", SaveFileFormat.SWF);

{{< /highlight >}}
```
### **没有查看器编程示例**
The SWF file created by these code snippets include an SWF viewer. Exclude the SWF viewer from the file using the following code.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Instantiate Diagram Object and open VSD file
Diagram diagram = new Diagram(dataDir + "ExportToSWFWithoutViewer.vsd");

// Instantiate the Save Options
SWFSaveOptions options = new SWFSaveOptions();

// Set Save format as SWF
options.SaveFormat = SaveFileFormat.SWF;

// Exclude the embedded viewer
options.ViewerIncluded = false;

// Save the resultant SWF file
diagram.Save(dataDir + "ExportToSWFWithoutViewer_out.swf", SaveFileFormat.SWF);

{{< /highlight >}}
```
## **Export a Diagram to XAML**
This article explains how to export a Microsoft Visio diagram to XAML (Extensible Application Markup Language) using [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

使用[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)类的构造函数读取 diagram 文件和 Save 方法将 diagram 导出为任何支持的图像格式。

将 VSD diagram 导出到 XAML：

1. 创建 Diagram 类的实例。
1. Call the class' Save method and set XAML as the export format.
### **Export Microsoft Visio Drawing to XAML**
The code sample show how to export a diagram to XAML using C#.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
// Load diagram
Diagram diagram = new Diagram(dataDir + "ExportToXAML.vsd");
// Save diagram
diagram.Save(dataDir + "ExportToXAML_out.xaml", SaveFileFormat.XAML);

{{< /highlight >}}
```
## **转换具有选择形状的绘图 Visio**
使用 Aspose.Diagram API，开发人员可以选择一组形状将 Visio 绘图转换为任何其他支持的格式。 RenderingSaveOptions 类提供了一个 Shapes 成员来维护一组形状。每个保存选项类都是 RenderingSaveOptions 类的扩展形式。

要导出具有选定形状的 Visio 绘图：

1. 创建 Diagram 类的实例。
1. 创建任何 SaveOption 类的实例以指定此处所述的设置：[指定 Visio 保存选项](https://docs.aspose.com/diagram/net/save-visio-document/#specifying-visio-save-options)
1. 调用 Diagram 类对象的 Save 方法并将保存选项类对象作为参数传递。
### **转换 Visio 具有选择形状的绘图编程示例**
代码示例显示了如何导出具有选择性 Visio 形状的绘图。

```
{{< highlight "csharp" >}}
// the path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance SVG save options class
SVGSaveOptions options = new SVGSaveOptions();
ShapeCollection shapes = options.Shapes;

// get shapes by page index and shape ID, and then add in the shape collection object
shapes.Add(diagram.Pages[0].Shapes.GetShape(1));
shapes.Add(diagram.Pages[0].Shapes.GetShape(2));

// save Visio drawing
diagram.Save(dataDir + "SelectiveShapes_out.svg", options);
{{< /highlight >}}
```