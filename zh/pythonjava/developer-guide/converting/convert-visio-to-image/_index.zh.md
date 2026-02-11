---
title: 将 Visio 转换为图像格式
linktitle: 将 Visio 转换为图像
type: docs
weight: 20
url: /zh/python-java/convert-visio-to-image/
description: This topic show you how to convert Visio to various images formats using Aspose.Diagram for Python via Java. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to PNG, JPEG, BMP images with a few lines of code.
---
## **将图表导出为图像文件格式**
This article explains how to export a Microsoft Visio diagram to an image using Aspose.Diagram for Python via Java.

Use the Diagram class' constructor to read the diagram files and the Save method to export the diagram to any supported image format.The image below shows a VSD file about to be saved to PNG format. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

**[示例 VSD 文件。](ExportToImage.vsd)**

要将 diagram 导出到图像：

- 创建 Diagram 类的实例。
- 调用 Diagram 类的 Save 方法并设置要导出的图像格式。输出的图像文件看起来像原始文件。

**输出PNG文件。**

![待办事项：图片_替代_文本](ExportToImage.png)
### **导出到图像文件编程示例**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSD file
diagram = Diagram("ExportToImage.vsd")

# Save as PNG
diagram.save("ExportToImage_Out.png", SaveFileFormat.PNG)

jpype.shutdownJVM()

{{< /highlight >}}
```

也可以将特定页面保存为图像，而不是整个文档：

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load diagram
diagram = Diagram("ExportToImage.vsd")

# Save diagram as PNG
options = ImageSaveOptions(SaveFileFormat.PNG)

# Save one page only, by page index
options.setPageIndex(0)

# Save resultant Image file
diagram.save("ExportPageToImage_Out.png", options)

jpype.shutdownJVM()

{{< /highlight >}}
```