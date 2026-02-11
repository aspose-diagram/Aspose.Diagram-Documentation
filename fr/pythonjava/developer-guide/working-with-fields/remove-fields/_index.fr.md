---
title: Supprimer les champs
type: docs
weight: 20
url: /fr/python-java/remove-fields/
description: Cette section explique comment supprimer des champs.
---
## **Supprimer le champ**
Aspose.Diagram for Python via Java lets you remove field to Microsoft Visio diagrams from within your own applications, without Microsoft Office Automation. 

L'objet Field représente un champ de texte dans une exécution de texte. La propriété field, exposée par la classe Shape prend en charge une collection d'objets Aspose.Diagram.Field.

### **Exemple de programmation**
Le morceau de code suivant supprime un champ dans shape.
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

