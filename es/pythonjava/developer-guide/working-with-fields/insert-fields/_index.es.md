---
title: Crear, Insertar campos
type: docs
weight: 10
url: /es/python-java/create-insert-fields/
description: Cómo crear, inserte campos usando Java Diagram API .
---
## **Insertar campo**
Aspose.Diagram for Python via Java lets you create and insert field to Microsoft Visio diagrams from within your own applications, without Microsoft Office Automation. 

### **Ejemplo de programación**
El siguiente fragmento de código inserta un campo en forma.

{{< highlight python >}}
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


