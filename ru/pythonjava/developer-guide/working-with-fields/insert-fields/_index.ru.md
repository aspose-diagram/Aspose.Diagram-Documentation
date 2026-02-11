---
title: Создать, Вставить поля
type: docs
weight: 10
url: /ru/python-java/create-insert-fields/
description: Как создавать, вставлять поля с помощью Java Diagram API.
---
## **Вставить поле**
 Aspose.Diagram для Python via Java позволяет создавать и вставлять поля в диаграммы Microsoft Visio из ваших собственных приложений без автоматизации.

### **Образец программирования**
Следующий фрагмент кода вставляет поле в shape.
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

