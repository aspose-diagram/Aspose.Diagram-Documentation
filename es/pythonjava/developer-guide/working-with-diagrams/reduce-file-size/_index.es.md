---
title: Reducir tamaño de archivo
type: docs
weight: 50
url: /es/python-java/reduce-file-size/
description: This section explains how to reduce file size from a diagram with Aspose.Diagram for Python via Java.
---
## **Reducir tamaño de archivo**
Aspose.Diagram for Python via Java API allows developers to remove hidden info from a diagram to reduce file size. 
 El objeto Page representa el área de dibujo de una página de primer plano o una página de fondo. Para reducir el tamaño del archivo, puede usar las propiedades RemoveHiddenInfoItem en**Eliminar información oculta ()** método de la clase Diagram. El siguiente ejemplo de código muestra cómo eliminar la información oculta de diagram.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Load a Visio diagram
diagram = Diagram("Drawing1.vsdx")

# Remove hidden information from diagram
diagram.removeHiddenInformation(RemoveHiddenInfoItem.SHAPES | RemoveHiddenInfoItem.MASTERS)

# save in the VSDX format
diagram.save("ReduceFileSize_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
