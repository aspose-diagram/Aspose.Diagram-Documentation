---
title: 减小文件大小
type: docs
weight: 50
url: /zh/python-java/reduce-file-size/
description: This section explains how to reduce file size from a diagram with Aspose.Diagram for Python via Java.
---
## **减小文件大小**
Aspose.Diagram for Python via Java API allows developers to remove hidden info from a diagram to reduce file size. 
 Page对象代表前景页面或背景页面的绘图区域。为了减小文件大小，可以使用RemoveHiddenInfoItem属性**移除隐藏信息()**Diagram 类的方法。下面的代码示例显示了如何从 diagram 中删除隐藏信息。

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Load a Visio diagram
diagram = Diagram("Drawing1.vsdx")

# Remove hidden information from diagram
diagram.removeHiddenInformation(RemoveHiddenInfoItem.SHAPES | RemoveHiddenInfoItem.MASTERS)

# save in the VSDX format
diagram.save("ReduceFileSize_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
