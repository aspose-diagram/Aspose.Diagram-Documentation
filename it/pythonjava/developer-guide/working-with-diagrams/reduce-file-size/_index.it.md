---
title: Riduci dimensione file
type: docs
weight: 50
url: /it/python-java/reduce-file-size/
description: This section explains how to reduce file size from a diagram with Aspose.Diagram for Python via Java.
---
## **Riduci dimensione file**
Aspose.Diagram for Python via Java API allows developers to remove hidden info from a diagram to reduce file size. 
 L'oggetto Page rappresenta l'area di disegno di una pagina in primo piano o di una pagina di sfondo. Per ridurre le dimensioni del file, è possibile utilizzare le proprietà RemoveHiddenInfoItem in**RimuoviInformazioni Nascoste()** metodo della classe Diagram. L'esempio di codice seguente mostra come rimuovere le informazioni nascoste da diagram.

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
