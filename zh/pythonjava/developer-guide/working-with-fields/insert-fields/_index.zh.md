---
title: 创建、插入字段
type: docs
weight: 10
url: /zh/python-java/create-insert-fields/
description: 如何使用 Java Diagram API 创建、插入字段。
---
## **插入字段**
Aspose.Diagram for Python via Java lets you create and insert field to Microsoft Visio diagrams from within your own applications, without Microsoft Office Automation. 

### **编程范例**
下面的一段代码在 shape 中插入一个字段。

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load a Visio diagram
diagram = Diagram("Drawing1.vsdx")

# Get page by name
page = diagram.getPages().getPage("Page-1")

# Get Visio Shape
shape = page.getShapes().get(0)
# Insert field
fld = Field()
fld.getValue().setVal("1")
shape.getFields().add(fld)

# Save diagram 
diagram.save("InsertField_out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}


