---
title: Felder entfernen
type: docs
weight: 20
url: /de/python-java/remove-fields/
description: In diesem Abschnitt wird erläutert, wie Felder entfernt werden.
---
## **Feld entfernen**
Aspose.Diagram for Python via Java lets you remove field to Microsoft Visio diagrams from within your own applications, without Microsoft Office Automation. 

Das Field-Objekt repräsentiert ein Textfeld in einem Textlauf. Die field-Eigenschaft, die von der Shape-Klasse verfügbar gemacht wird, unterstützt eine Sammlung von Aspose.Diagram.Field-Objekten.

### **Programmierbeispiel**
Der folgende Codeabschnitt entfernt ein Feld in shape.

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


