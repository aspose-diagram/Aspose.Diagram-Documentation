---
title: Eliminar campos
type: docs
weight: 20
url: /es/python-java/remove-fields/
description: Esta sección explica cómo eliminar campos.
---
## **Eliminar campo**
Aspose.Diagram for Python via Java lets you remove field to Microsoft Visio diagrams from within your own applications, without Microsoft Office Automation. 

El objeto Field representa un campo de texto en una ejecución de texto. La propiedad de campo, expuesta por la clase Shape, admite una colección de objetos Aspose.Diagram.Field.

### **Ejemplo de programación**
El siguiente fragmento de código elimina un campo en forma.

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


