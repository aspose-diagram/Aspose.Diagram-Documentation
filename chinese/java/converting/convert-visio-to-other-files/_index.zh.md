---
title:  Visio转其他格式
linktitle:  Visio转其他格式
type: docs
weight: 40
url: /zh/java/convert-visio-to-other-files/
description: 本主题向您展示如何将 Aspose.Diagram 允许将 Visio 转换为 SVG、XPS、XML、XAML 格式。使用几行代码将 VSD、VSS、VDW、VST、VSDX、VSSX、VSTX、VSDM、VSTM、VSSM 转换为 SVG、XPS、XML、XAML。
---
## **导出为 XML**
本文介绍了如何使用 将 Microsoft Visio diagram 导出到 XML[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

- VDX 定义了一个 XML diagram。
- VTX 定义了一个 XML 模板。
- VSX 定义了一个 XML 模板。

这[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram)类的构造函数读取 diagram，Save 方法用于以不同的文件格式保存或导出 diagram。本文中的代码片段显示了如何使用 Save 方法将 Visio 文件保存到[VDX](/diagram/zh/java/how-to-convert-a-visio-diagram/), [VTX](/diagram/zh/java/how-to-convert-a-visio-diagram/)和[VSX](/diagram/zh/java/how-to-convert-a-visio-diagram/).

下图显示了在下面的代码片段中导出的 diagram。导出的文件显示在每个代码片段之前。

**A Microsoft Visio diagram 即将出口。**

![待办事项：图片_替代_文本](http://i.imgur.com/XWajazh.png)
### **出口 VSD 到 VDX**
VDX 是一种基于架构的 XML 文件格式，可让您以 Microsoft Visio 以外的产品可以读取的格式保存图表。这是一种在软件应用程序之间传输图表和保留可编辑数据的有用格式。

将 VSD diagram 导出到 VDX：

1. 创建 Diagram 类的实例。
1. 调用Diagram类的Save方法将Visio绘图文件写入VDX。

**导出的 VDX 文件。**

![待办事项：图片_替代_文本](http://i.imgur.com/OJ1jpgh.png)
### **从 VSD 导出到 VSX**
VSX 是一种用于定义模板的 XML 格式，模板是构建 diagram 的基本对象。当 Visio 文件转换为 VSX 时，仅导出模板。

将 VSD diagram 导出到 VSX：

- 创建 Diagram 类的实例。
- 调用Diagram类的Save方法将Visio绘图文件写入VSX。

下图显示了输出 VSX 文件。请注意，导出的是 diagram 中使用的模板，而不是 diagram 本身。

**导出的 VSX 文件。**

![待办事项：图片_替代_文本](http://i.imgur.com/gkZrxCN.png)
### **导出 VSD 到 VTX**
TVX 是模板文件的 XML 表示，并存储文档的设置。

将 VSD diagram 导出到 VTX：

1. 创建 Diagram 类的实例。
1. 调用diagram类的Save方法写入VTX格式的Visio图形文件。

下图显示了输出 VTX 文件。

**输出VTX文件。**

![待办事项：图片_替代_文本](http://i.imgur.com/E6pUvGD.jpg)
### **导出到 XML 编程示例**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToXML-ExportToXML.java" >}}
## **导出到 XPS**
本文介绍了如何使用 将 Microsoft Visio diagram 导出到 XPS[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.
使用[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)类的构造函数读取 diagram 文件和 Save 方法将 diagram 导出为任何支持的图像格式。

本文中的代码片段将下面的 diagram 作为输入。您也可以使用其他 diagram 格式（VSS、VSSX、VSSM、VDX、VST、VSTX、VSTM、VDX、VTX 或 VSX）。

**源文档。**

![待办事项：图片_替代_文本](http://i.imgur.com/P3gaA34.png)

要将 VSD diagram 导出到 XPS：

1. 创建 Diagram 类的实例。
1. 调用 Diagram 类的 Save 方法并将 XPS 设置为输出格式。

下图显示了输出的 XPS 文件。

**输出 XPS。**

![待办事项：图片_替代_文本](http://i.imgur.com/1ESRxSy.png)
### **导出到 XPS 编程示例**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToXPS-ExportToXPS.java" >}}
## **将 Diagram 导出为 SVG**
本文介绍了如何使用 将 Microsoft Visio diagram 导出为 SVG（可缩放矢量图形）[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

使用[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram)类的构造函数读取 diagram 文件和 Save 方法将 diagram 导出为任何支持的图像格式。

要将 VSD diagram 导出为 SVG，请执行以下步骤：

1. 创建 Diagram 类的实例。
1. 调用类的 Save 方法并将 SVG 设置为导出格式。
### **将 Diagram 导出为 SVG 编程示例**
代码示例展示了如何使用 Java 将 diagram 导出为 SVG。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToSVG-ExportToSVG.java" >}}
## **将 Diagram 导出到 XAML**
本文介绍如何将 Microsoft Visio diagram 导出到 XAML（可扩展应用程序标记语言）使用[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

使用[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram)类的构造函数读取 diagram 文件和 Save 方法将 diagram 导出为任何支持的图像格式。

要将 VSD diagram 导出到 XAML：

1. 创建 Diagram 类的实例。
1. 调用类的 Save 方法并将 XAML 设置为导出格式。
### **导出到 XAML 编程示例**
代码示例展示了如何使用 Java 将 diagram 导出到 XAML。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToXAML-ExportToXAML.java" >}}

## **转换具有选择形状的绘图 Visio**
使用 Aspose.Diagram API，开发人员可以选择一组形状将 Visio 绘图转换为任何其他支持的格式。 RenderingSaveOptions 类提供了一个 Shapes 成员来维护一组形状。每个保存选项类都是 RenderingSaveOptions 类的扩展形式。

要导出具有选定形状的 Visio 绘图：

1. 创建 Diagram 类的实例。
1. 创建任何 SaveOption 类的实例以指定此处所述的设置：[指定 Visio 保存选项](https://docs.aspose.com/diagram/java/save-a-visio-drawing-to-pdf-html-and-other-formats/#specifying-visio-save-options)
1. 调用 Diagram 类对象的保存方法并将保存选项类对象作为参数传递。
### **转换 Visio 具有选择形状的绘图编程示例**
代码示例显示了如何导出具有选择性 Visio 形状的绘图。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ConvertVisioWithSelectiveShapes.Java" >}}