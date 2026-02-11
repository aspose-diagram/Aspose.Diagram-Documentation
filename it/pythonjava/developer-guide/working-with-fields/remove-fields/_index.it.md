---
title: Rimuovi campi
type: docs
weight: 20
url: /it/python-java/remove-fields/
description: Questa sezione spiega come rimuovere i campi.
---
## **Rimuovi campo**
Aspose.Diagram for Python via Java lets you remove field to Microsoft Visio diagrams from within your own applications, without Microsoft Office Automation. 

L'oggetto Field rappresenta il campo di testo in un'esecuzione di testo. La proprietà field, esposta dalla classe Shape, supporta una raccolta di oggetti Aspose.Diagram.Field.

### **Esempio di programmazione**
Il seguente pezzo di codice rimuove un campo in shape.
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

