---
title: Обновить поля
type: docs
weight: 20
url: /ru/python-java/update-fields/
description: В этом разделе объясняется, как обновлять поля.
---
## **Обновить поле**
Aspose.Diagram для Python via Java позволяет обновлять поля до Microsoft Visio диаграмм из ваших собственных приложений, без автоматизации.

Объект Field представляет собой текстовое поле в текстовом прогоне. Свойство field, предоставляемое классом Shape, поддерживает набор объектов Aspose.Diagram.Field.

### **Образец программирования**
Следующий фрагмент кода обновляет поле в форме.
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
