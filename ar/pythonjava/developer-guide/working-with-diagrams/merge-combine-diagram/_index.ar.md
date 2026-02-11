---
title: دمج الجمع Diagram
type: docs
weight: 30
url: /ar/python-java/merge-combine-diagram/
description: يشرح هذا القسم كيفية دمج ملف visio
---
## **سيناريوهات الاستخدام الممكنة**

Aspose.Diagram لـ Python via Java يسمح لك بدمج ملفين visio في ملف واحد.
Aspose.Diagram لـ Python via Java API له فئة Diagram التي تمثل رسم Visio.
باستخدام الطريقة**يجمع** في فئة Diagram لدمج الرسوم البيانية.

## **عينة من الرموز**
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

# Load another Visio diagram
diagram2 = Diagram("DrawingFlowChart.vsdx")

diagram2.combine(diagram)

# save in the VSDX format
diagram2.save("CombineDiagram_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
