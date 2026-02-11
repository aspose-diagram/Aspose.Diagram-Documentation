---
title: Uppdatera fält
type: docs
weight: 20
url: /sv/python-java/update-fields/
description: Det här avsnittet förklarar hur du uppdaterar fält.
---
## **Uppdatera fält**
Aspose.Diagram för Python via Java låter dig uppdatera fältet till Microsoft Visio diagram från dina egna applikationer, utan Microsoft Office Automation.

Fältobjektet representerar textfält i en textkörning. Fältegenskapen, exponerad av Shape-klassen stöder en samling Aspose.Diagram.Field-objekt.

### **Programmeringsexempel**
Följande kod uppdaterar ett fält i form.
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
