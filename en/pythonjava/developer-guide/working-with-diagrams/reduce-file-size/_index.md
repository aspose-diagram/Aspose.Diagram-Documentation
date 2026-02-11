---
title: Reduce File Size
type: docs
weight: 50
url: /python-java/reduce-file-size/
description: This section explains how to reduce file size from a diagram with Aspose.Diagram for Python via Java.
---

## **Reduce File Size**
Aspose.Diagram for Python via Java API allows developers to remove hidden info from a diagram to reduce file size. 
The Page object represents the drawing area of a foreground page or a background page.In order to reduce file size, you can use RemoveHiddenInfoItem properties in  **RemoveHiddenInformation()** method of Diagram class. The code example below shows how to remove hidden info from diagram.

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
