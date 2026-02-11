---
title: Unisci Combina Diagram
type: docs
weight: 30
url: /it/python-java/merge-combine-diagram/
description: Questa sezione spiega come combinare il file visio
---
## **Possibili scenari di utilizzo**

Aspose.Diagram for Python via Java allows you to combine two visio files to one. 
Aspose.Diagram for Python via Java API has the Diagram class that represents a Visio drawing.
Usando il metodo**Combina** nella classe Diagram per combinare i diagrammi.

## **Codice di esempio**

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

