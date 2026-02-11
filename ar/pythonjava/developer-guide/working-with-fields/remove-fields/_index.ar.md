---
title: إزالة الحقول
type: docs
weight: 20
url: /ar/python-java/remove-fields/
description: يشرح هذا القسم كيفية إزالة الحقول.
---
## **إزالة الحقل**
 يتيح لك Aspose.Diagram لـ Python via Java إزالة الحقل إلى المخططات Microsoft Visio من داخل التطبيقات الخاصة بك ، بدون أتمتة Microsoft Office.

يمثل كائن الحقل الحقل النصي في تشغيل النص. تدعم خاصية الحقل ، المعروضة بواسطة فئة الشكل مجموعة من Aspose.Diagram.Field كائنات.

### **عينة البرمجة**
الجزء التالي من التعليمات البرمجية يزيل حقلاً في الشكل.

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


