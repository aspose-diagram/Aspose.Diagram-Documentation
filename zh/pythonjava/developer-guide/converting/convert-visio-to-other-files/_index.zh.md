---
title:  Visio转其他格式
linktitle:  Visio转其他格式
type: docs
weight: 40
url: /zh/python-java/convert-visio-to-other-files/
description: This topic show you how to convert Visio to SVG,XPS,XML,XAML formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to SVG,XPS,XML,XAML with a few lines of code.
---
**[要导出的 Microsoft Visio diagram。](ExportToXML.vsd)**

## **导出为 XML**
This article explains how to export a Microsoft Visio diagram to XML using Aspose.Diagram for Python via Java.

- VDX 定义了一个 XML diagram。
- VTX 定义了一个 XML 模板。
- VSX 定义了一个 XML 模板。

Diagram 类的构造函数读取 diagram，Save 方法用于以不同的文件格式保存或导出 diagram。本文中的代码片段展示了如何使用 Save 方法将 Visio 文件保存为 VDX、VTX 和 VSX 格式。

### **出口 VSD 到 VDX**
VDX 是一种基于架构的 XML 文件格式，可让您以 Microsoft Visio 以外的产品可以读取的格式保存图表。这是一种在软件应用程序之间传输图表和保留可编辑数据的有用格式。

将 VSD diagram 导出到 VDX：

1. 创建 Diagram 类的实例。
1. 调用Diagram类的Save方法将Visio绘图文件写入VDX。

### **从 VSD 导出到 VSX**
VSX 是一种用于定义模板的 XML 格式，模板是构建 diagram 的基本对象。当 Visio 文件转换为 VSX 时，仅导出模板。

将 VSD diagram 导出到 VSX：

- 创建 Diagram 类的实例。
- 调用Diagram类的Save方法将Visio绘图文件写入VSX。

下图显示了输出 VSX 文件。请注意，导出的是 diagram 中使用的模板，而不是 diagram 本身。

### **导出 VSD 到 VTX**
TVX 是模板文件的 XML 表示，并存储文档的设置。

将 VSD diagram 导出到 VTX：

1. 创建 Diagram 类的实例。
1. 调用diagram类的Save方法写入VTX格式的Visio图形文件。

下图显示了输出 VTX 文件。

### **导出到 XML 编程示例**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# 1. Exporting VSDX to VDX
# Call the diagram constructor to load diagram from a VSD file
diagram = Diagram("ExportToXML.vsd")

# Save input VSD as VDX
diagram.save("ExportToXML_Out.vdx", SaveFileFormat.VDX)

# 2. Exporting from VSD to VSX
# Call the diagram constructor to load diagram from a VSD file
        
# Save input VSD as VSX
diagram.save("ExportToXML_Out.vsx", SaveFileFormat.VSX)
        
# 3. Export VSD to VTX
# Save input VSD as VTX
diagram.save("ExportToXML_Out.vtx", SaveFileFormat.VTX)

jpype.shutdownJVM()

{{< /highlight >}}
```

## **Exporting to XPS**
This article explains how to export a Microsoft Visio diagram to XPS using Aspose.Diagram for Python via Java.
使用 Diagram 类的构造函数读取 diagram 文件，并使用 Save 方法将 diagram 导出为任何支持的图像格式。

The code snippets in this article takes the diagram below as an input. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

To export VSD diagram to XPS:

1. 创建 Diagram 类的实例。
1. Call the Diagram class' Save method and set XPS as the output format.

下图显示了输出 XPS 文件。

### **Exporting to XPS Programming Sample**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSD file
diagram = Diagram("ExportToXPS.vsd")

# Save as XPS
diagram.save("ExportToXPS_Out.xps", SaveFileFormat.XPS)

jpype.shutdownJVM()

{{< /highlight >}}
```

## **Exporting a Diagram to SVG**
This article explains how to export a Microsoft Visio diagram to SVG (Scalable Vector Graphics) using Aspose.Diagram for Python via Java.

使用 Diagram 类的构造函数读取 diagram 文件，并使用 Save 方法将 diagram 导出为任何支持的图像格式。

To export VSD diagram to SVG, perform the following steps:

1. 创建 Diagram 类的实例。
1. Call the class' Save method and set SVG as the export format.

### **Exporting Diagram to SVG Programming Sample**
The code samples show how to export a diagram to SVG using Java.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# call the diagram constructor to load diagram from a VSD file
diagram = Diagram("ExportToSVG.vsd")

# Save as SVG
diagram.save("ExportToSVG_Out.svg", SaveFileFormat.SVG)

jpype.shutdownJVM()

{{< /highlight >}}
```

## **Exporting a Diagram to XAML**
This article explains how to export a Microsoft Visio diagram to XAML (Extensible Application Markup Language) using Aspose.Diagram for Python via Java.

使用 Diagram 类的构造函数读取 diagram 文件，并使用 Save 方法将 diagram 导出为任何支持的图像格式。

将 VSD diagram 导出到 XAML：

1. 创建 Diagram 类的实例。
1. Call the class' Save method and set XAML as the export format.

### **Exporting to XAML Programming Sample**
The code sample show how to export a diagram to XAML using Java.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# call the diagram constructor to load diagram from a VSD file
diagram = Diagram("ExportToXAML.vsd")

# save as XAML
diagram.save("ExportToXAML_Out.xaml", SaveFileFormat.XAML)

jpype.shutdownJVM()

{{< /highlight >}}
```

## **转换具有选择形状的绘图 Visio**
使用 Aspose.Diagram API，开发人员可以选择一组形状将 Visio 绘图转换为任何其他支持的格式。 RenderingSaveOptions 类提供了一个 Shapes 成员来维护一组形状。每个保存选项类都是 RenderingSaveOptions 类的扩展形式。

要导出具有选定形状的 Visio 绘图：

1. 创建 Diagram 类的实例。
1. 创建任何 SaveOption 类的实例以指定所叙述的设置
1. 调用 Diagram 类对象的保存方法并将保存选项类对象作为参数传递。

### **转换 Visio 具有选择形状的绘图编程示例**
代码示例显示了如何导出具有选择性 Visio 形状的绘图。

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# call the diagram constructor to load diagram from a VSD file
diagram = Diagram("DrawingSimple.vsdx")

# create an instance SVG save options class
options = SVGSaveOptions()
shapes = options.getShapes()

# get shapes by page index and shape ID, and then add in the shape collection object
shapes.add(diagram.getPages().get(0).getShapes().getShape(1))
shapes.add(diagram.getPages().get(0).getShapes().getShape(2))

# save Visio drawing
diagram.save("SelectiveShapes_out.svg", options)

jpype.shutdownJVM()

{{< /highlight >}}
```