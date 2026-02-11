---
title: Fusionner Combiner Diagram
type: docs
weight: 30
url: /fr/python-java/merge-combine-diagram/
description: Cette section explique comment combiner le fichier visio
---
## **Scénarios d'utilisation possibles**

Aspose.Diagram for Python via Java allows you to combine two visio files to one. 
Aspose.Diagram for Python via Java API has the Diagram class that represents a Visio drawing.
En utilisant la méthode**Combiner** dans la classe Diagram pour combiner des diagrammes.

## **Exemple de code**

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

