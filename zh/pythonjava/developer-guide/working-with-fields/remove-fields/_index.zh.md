---
title: 删除字段
type: docs
weight: 20
url: /zh/python-java/remove-fields/
description: 本节介绍如何删除字段。
---
## **删除字段**
Aspose.Diagram for Python via Java lets you remove field to Microsoft Visio diagrams from within your own applications, without Microsoft Office Automation. 

Field 对象表示文本运行中的文本字段。 Shape 类公开的字段属性支持 Aspose.Diagram.Field 对象的集合。

### **编程范例**
下面的一段代码删除了形状中的一个字段。

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load a Visio diagram
diagram = Diagram("InsertField_out.vsdx")

# Get page by name
page = diagram.getPages().getPage("Page-1")

# Get Visio Shape
shape = page.getShapes().get(0)

fld = shape.getFields().get(0)
# Remove field of shape
shape.getFields().remove(fld)

# Save diagram
diagram.save("RemoveField_out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}


