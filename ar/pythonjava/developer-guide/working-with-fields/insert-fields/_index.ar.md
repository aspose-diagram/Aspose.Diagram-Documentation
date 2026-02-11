---
title: إنشاء وإدراج الحقول
type: docs
weight: 10
url: /ar/python-java/create-insert-fields/
description: كيفية إنشاء وإدخال الحقول باستخدام Java Diagram API.
---
## **أدخل الحقل**
 يتيح لك Aspose.Diagram لـ Python via Java إنشاء وإدراج حقل للرسومات التخطيطية Microsoft Visio من داخل التطبيقات الخاصة بك ، بدون أتمتة Microsoft Office.

### **عينة البرمجة**
الجزء التالي من التعليمات البرمجية إدراج حقل في الشكل.
```
{{< highlight "python" >}}
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
```

