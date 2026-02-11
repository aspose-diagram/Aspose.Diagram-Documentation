---
title: Ta bort fält
type: docs
weight: 20
url: /sv/python-java/remove-fields/
description: Det här avsnittet förklarar hur man tar bort fält.
---
## **Ta bort fält**
 Aspose.Diagram för Python via Java låter dig ta bort fält till Microsoft Visio diagram från dina egna applikationer, utan Microsoft Office Automation.

Fältobjektet representerar textfält i en textkörning. Fältegenskapen, exponerad av Shape-klassen stöder en samling Aspose.Diagram.Field-objekt.

### **Programmeringsexempel**
Följande kodbit tar bort ett fält i form.
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
# Remove field of shape
shape.getFields().remove(fld)

# Save diagram
diagram.save("RemoveField_out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```

