---
title: Удалить поля
type: docs
weight: 20
url: /ru/python-java/remove-fields/
description: В этом разделе объясняется, как удалить поля.
---
## **Удалить поле**
 Aspose.Diagram для Python via Java позволяет удалить поля для Microsoft Visio диаграмм из ваших собственных приложений без автоматизации.

Объект Field представляет собой текстовое поле в текстовом прогоне. Свойство field, предоставляемое классом Shape, поддерживает набор объектов Aspose.Diagram.Field.

### **Образец программирования**
Следующий фрагмент кода удаляет поле в форме.

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


