---
title:  Visio转其他格式
linktitle:  Visio转其他格式
type: docs
weight: 40
url: /zh/python-net/convert-visio-to-other-files/
description: This topic show you how to Aspose.Diagram allows to convert Visio to SVG,XPS,XML,XAML formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to SVG,XPS,XML,XAML with a few lines of code.
---
## **导出为 XML**
### **Export Microsoft Visio Drawing to PDF**
The code samples show how to export Microsoft Visio Drawing to PDF using C#.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToPdf.py" >}}

本文介绍了如何使用 将 Microsoft Visio diagram 导出到 XML[Aspose.Diagram for Python via .NET](https://products.aspose.com/diagram/python-net/) API.

- VDX 定义了一个 XML diagram。
- VTX 定义了一个 XML 模板。
- VSX 定义了一个 XML 模板。

 [Diagram] 类的构造函数读取 diagram，Save 方法用于以不同的文件格式保存或导出 diagram。本文中的代码片段显示了如何使用 Save 方法将 Visio 文件保存到[VDX](https://docs.aspose.com/diagram/python-net/save-visio-document/), [VTX](https://docs.aspose.com/diagram/python-net/save-visio-document/)和[VSX](https://docs.aspose.com/diagram/python-net/save-visio-document/).

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

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToXml.py" >}}

## **Export to XPS**
This article explains how to export a Microsoft Visio diagram to XPS using [Aspose.Diagram for Python via .NET](https://products.aspose.com/diagram/python-net/) API.
使用 [Diagram] 类的构造函数读取 diagram 文件，并使用 Save 方法将 diagram 导出为任何支持的图像格式。

The code snippets in this article takes the diagram below as an input. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

|**源文档。**|
|:- |
|![待办事项：图片_替代_文本](how-to-convert-a-visio-diagram_5.png)|


To export VSD diagram to XPS:

1. 创建 Diagram 类的实例。
1. Call the Diagram class' Save method and set XPS as the output format.
### **Export Microsoft Visio Drawing to XPS**
The code samples show how to export Microsoft Visio Drawing to XPS using C#.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToXps.py" >}}

## **Export a Diagram to SVG**
This article explains how to export a Microsoft Visio diagram to SVG (Scalable Vector Graphics) using [Aspose.Diagram for Python via .NET](https://products.aspose.com/diagram/python-net/) API.

使用 [Diagram] 类的构造函数读取 diagram 文件，并使用 Save 方法将 diagram 导出为任何支持的图像格式。

To export VSD diagram to SVG, perform the following steps:

1. 创建 Diagram 类的实例。
1. Call the class' Save method and set SVG as the export format.
### **Export Microsoft Visio Drawing to SVG**
The code samples show how to export a diagram to SVG using C#.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToSvg.py" >}}

要导出具有选定形状的 Visio 绘图：

1. 创建 Diagram 类的实例。
1. 创建任何 SaveOption 类的实例以指定此处所述的设置：[指定 Visio 保存选项](https://docs.aspose.com/diagram/python-net/save-visio-document/#specifying-visio-save-options)
1. 调用 Diagram 类对象的 Save 方法并将保存选项类对象作为参数传递。
### **转换 Visio 具有选择形状的绘图编程示例**
代码示例显示了如何导出具有选择性 Visio 形状的绘图。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-PythonNet-ConvertVisioWithSelectiveShapes.py" >}}