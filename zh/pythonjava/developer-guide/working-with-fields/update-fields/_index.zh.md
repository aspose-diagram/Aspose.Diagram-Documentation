---
title: 更新字段
type: docs
weight: 20
url: /zh/python-java/update-fields/
description: 本节介绍如何更新字段。
---
## **更新字段**
Aspose.Diagram for Python via Java lets you update field to Microsoft Visio diagrams from within your own applications, without Microsoft Office Automation. 

Field 对象表示文本运行中的文本字段。 Shape 类公开的字段属性支持 Aspose.Diagram.Field 对象的集合。

### **编程范例**
下面的一段代码更新了一个字段的形状。
```
{{< highlight "python" >}}
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
# Update format of field
fld.getFormat().setVal("")
fld.getFormat().getUfev().setUnit(MeasureConst.UNDEFINED)
fld.getFormat().getUfev().setF("")

# Update value of field
fld.getValue().setVal("1")
fld.getValue().getUfev().setF("")
fld.getValue().getUfev().setUnit(MeasureConst.UNDEFINED)

# Save diagram 
diagram.save("UpdateField_out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
