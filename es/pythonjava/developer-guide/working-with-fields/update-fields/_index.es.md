---
title: Actualizar campos
type: docs
weight: 20
url: /es/python-java/update-fields/
description: Esta sección explica cómo actualizar los campos.
---
## **Actualizar campo**
Aspose.Diagram for Python via Java lets you update field to Microsoft Visio diagrams from within your own applications, without Microsoft Office Automation. 

El objeto Field representa un campo de texto en una ejecución de texto. La propiedad de campo, expuesta por la clase Shape, admite una colección de objetos Aspose.Diagram.Field.

### **Ejemplo de programación**
El siguiente fragmento de código actualiza un campo en forma.
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
