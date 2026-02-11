---
title: تحديث الحقول
type: docs
weight: 20
url: /ar/python-java/update-fields/
description: يوضح هذا القسم كيفية تحديث الحقول.
---
## **تحديث الميدان**
يتيح لك Aspose.Diagram لـ Python via Java تحديث الحقل إلى الرسوم البيانية Microsoft Visio من داخل التطبيقات الخاصة بك ، بدون أتمتة Microsoft Office.

يمثل كائن الحقل الحقل النصي في تشغيل النص. تدعم خاصية الحقل ، المعروضة بواسطة فئة الشكل مجموعة من Aspose.Diagram.Field كائنات.

### **عينة البرمجة**
يقوم الجزء التالي من التعليمات البرمجية بتحديث حقل في الشكل.

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

