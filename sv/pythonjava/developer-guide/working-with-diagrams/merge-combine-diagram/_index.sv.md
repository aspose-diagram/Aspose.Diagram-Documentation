---
title: Slå samman Kombinera Diagram
type: docs
weight: 30
url: /sv/python-java/merge-combine-diagram/
description: Det här avsnittet förklarar hur man kombinerar visio-filen
---
## **Möjliga användningsscenarier**

Aspose.Diagram för Python via Java låter dig kombinera två visio-filer till en.
Aspose.Diagram för Python via Java API har klassen Diagram som representerar en Visio ritning.
Använder metoden**Kombinera** i Diagram klass för att kombinera diagram.

## **Exempelkod**

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Load a Visio diagram
diagram = Diagram("Drawing1.vsdx")

# Load another Visio diagram
diagram2 = Diagram("DrawingFlowChart.vsdx")

diagram2.combine(diagram)

# save in the VSDX format
diagram2.save("CombineDiagram_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

