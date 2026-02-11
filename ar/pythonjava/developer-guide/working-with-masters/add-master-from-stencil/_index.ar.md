---
title: إضافة ماجستير من الاستنسل
type: docs
weight: 30
url: /ar/python-java/add-master-from-stencil/
description: يشرح هذا القسم كيفية إضافة عنصر رئيسي من الاستنسل
---
## **سيناريوهات الاستخدام الممكنة**

 Aspose.Diagram لـ Python via Java يسمح لك بإضافة رئيسي من الاستنسل.
يحتوي Aspose.Diagram لـ Python via Java API على الفئة الرئيسية التي تمثل قالب شكل رسم Visio.
باستخدام الطريقة**addMaster** في فئة Diagram لإضافة ماستر من الاستنسل.

## **عينة من الرموز**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Load diagram
diagram = Diagram()

# Load stencil to a stream
templateFileName = "NetApp-FAS-series.vss"

# Add master with stencil file path and master id
diagram.addMaster(templateFileName, 2)

# Add master with stencil file path and master name
masterName = "FAS80xx rear empty"
diagram.addMaster(templateFileName, masterName)

# adds master to diagram from source diagram
src = Diagram(templateFileName)
diagram.addMaster(src, masterName)

# Adds shape with defined PinX and PinY.
diagram.addShape(2.0, 2.0, masterName, 0)
diagram.addShape(6.0, 6.0, masterName, 0)

diagram.save("AddMasterFromStencil_out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
