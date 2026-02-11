---
title: Update Fields
type: docs
weight: 20
url: /python-java/update-fields/
description: This section explains how to update fields.
---

## **Update Field**
Aspose.Diagram for Python via Java lets you update field to Microsoft Visio diagrams from within your own applications, without Microsoft Office Automation. 

The Field object represents text field in a text run. The field property, exposed by the Shape class supports a collection of Aspose.Diagram.Field objects.

### **Programming Sample**
The following piece of code update a field in shape.

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

