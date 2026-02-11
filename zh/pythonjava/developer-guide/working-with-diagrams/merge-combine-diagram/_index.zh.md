---
title: 合并组合 Diagram
type: docs
weight: 30
url: /zh/python-java/merge-combine-diagram/
description: 本节说明如何合并 visio 文件
---
## **可能的使用场景**

Aspose.Diagram for Python via Java allows you to combine two visio files to one. 
Aspose.Diagram for Python via Java API has the Diagram class that represents a Visio drawing.
使用方法**结合**在 Diagram 类中组合图表。

## **示例代码**

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Load a Visio diagram
diagram = Diagram("Drawing1.vsdx")

# Load another Visio diagram
diagram2 = Diagram("DrawingFlowChart.vsdx")

diagram2.combine(diagram)

# save in the VSDX format
diagram2.save("CombineDiagram_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

