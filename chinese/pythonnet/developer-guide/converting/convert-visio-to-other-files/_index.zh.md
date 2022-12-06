---
title:  Visio转其他格式
linktitle:  Visio转其他格式
type: docs
weight: 40
url: /zh/python-net/convert-visio-to-other-files/
description: 本主题向您展示如何将 Aspose.Diagram 允许将 Visio 转换为 SVG、XPS、XML、XAML 格式。使用几行代码将 VSD、VSS、VDW、VST、VSDX、VSSX、VSTX、VSDM、VSTM、VSSM 转换为 SVG、XPS、XML、XAML。
---
## **导出为 XML**
### **将 Microsoft Visio 图纸导出为 PDF**
代码示例显示了如何使用 C# 将 Microsoft Visio 绘图导出为 PDF。

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToPdf.py" >}}

本文介绍了如何使用 将 Microsoft Visio diagram 导出到 XML[Aspose.Diagram 为 Python 通过 .NET](https://products.aspose.com/diagram/python-net/) API.

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

## **导出到 XPS**
本文介绍了如何使用 将 Microsoft Visio diagram 导出到 XPS[Aspose.Diagram 为 Python 通过 .NET](https://products.aspose.com/diagram/python-net/) API.
使用 [Diagram] 类的构造函数读取 diagram 文件，并使用 Save 方法将 diagram 导出为任何支持的图像格式。

本文中的代码片段将下面的 diagram 作为输入。您也可以使用其他 diagram 格式（VSS、VSSX、VSSM、VDX、VST、VSTX、VDX、VTX 或 VSX）。

|**源文档。**|
|:- |
|![待办事项：图片_替代_文本](how-to-convert-a-visio-diagram_5.png)|


要将 VSD diagram 导出到 XPS：

1. 创建 Diagram 类的实例。
1. 调用 Diagram 类的 Save 方法并将 XPS 设置为输出格式。
### **将 Microsoft Visio 绘图导出到 XPS**
代码示例显示了如何使用 C# 将 Microsoft Visio 绘图导出到 XPS。

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToXps.py" >}}

## **将 Diagram 导出为 SVG**
本文介绍了如何使用 将 Microsoft Visio diagram 导出为 SVG（可缩放矢量图形）[Aspose.Diagram 为 Python 通过 .NET](https://products.aspose.com/diagram/python-net/) API.

使用 [Diagram] 类的构造函数读取 diagram 文件，并使用 Save 方法将 diagram 导出为任何支持的图像格式。

要将 VSD diagram 导出为 SVG，请执行以下步骤：

1. 创建 Diagram 类的实例。
1. 调用类的 Save 方法并将 SVG 设置为导出格式。
### **导出 Microsoft Visio 绘图到 SVG**
代码示例展示了如何使用 C# 将 diagram 导出为 SVG。

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToSvg.py" >}}

要导出具有选定形状的 Visio 绘图：

1. 创建 Diagram 类的实例。
1. 创建任何 SaveOption 类的实例以指定此处所述的设置：[指定 Visio 保存选项](https://docs.aspose.com/diagram/python-net/save-visio-document/#specifying-visio-save-options)
1. 调用 Diagram 类对象的 Save 方法并将保存选项类对象作为参数传递。
### **转换 Visio 具有选择形状的绘图编程示例**
代码示例显示了如何导出具有选择性 Visio 形状的绘图。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-PythonNet-ConvertVisioWithSelectiveShapes.py" >}}