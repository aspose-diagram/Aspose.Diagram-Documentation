---
title: Skapa, infoga fält
type: docs
weight: 10
url: /sv/python-java/create-insert-fields/
description: Så här skapar du, infoga fält med Java Diagram API .
---
## **Infoga fält**
 Aspose.Diagram för Python via Java låter dig skapa och infoga fält till Microsoft Visio diagram från dina egna applikationer, utan Microsoft 081617.

### **Programmeringsexempel**
Följande kodbit infogar ett fält i form.
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

