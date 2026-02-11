---
title: Dateigröße reduzieren
type: docs
weight: 50
url: /de/python-java/reduce-file-size/
description: This section explains how to reduce file size from a diagram with Aspose.Diagram for Python via Java.
---
## **Dateigröße reduzieren**
Aspose.Diagram for Python via Java API allows developers to remove hidden info from a diagram to reduce file size. 
 Das Page-Objekt stellt den Zeichenbereich einer Vordergrundseite oder einer Hintergrundseite dar. Um die Dateigröße zu reduzieren, können Sie RemoveHiddenInfoItem-Eigenschaften in verwenden**RemoveHiddenInformation()** Methode der Klasse Diagram. Das folgende Codebeispiel zeigt, wie versteckte Informationen aus diagram entfernt werden.


{{< highlight python >}}
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

