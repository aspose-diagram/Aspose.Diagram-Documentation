---
title: Master aus Schablone hinzufügen
type: docs
weight: 30
url: /de/python-java/add-master-from-stencil/
description: In diesem Abschnitt wird erläutert, wie Sie einen Master aus einer Schablone hinzufügen
---
## **Mögliche Nutzungsszenarien**

Aspose.Diagram for Python via Java allows you to add master from stencil. 
Aspose.Diagram for Python via Java API has the Master class that represents a Visio drawing shape template.
Mit der Methode**addMaster** in der Klasse Diagram, um Master aus Schablone hinzuzufügen.

## **Beispielcode**

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Load diagram
diagram = Diagram()

# Load stencil to a stream
templateFileName = "NetApp-FAS-series.vss"

# Add master with stencil file path and master id
diagram.addMaster(templateFileName, 2)

# Add master with stencil file path and master name
masterName = "FAS80xx rear empty"
diagram.addMaster(templateFileName, masterName)

# adds master to diagram from source diagram
src = Diagram(templateFileName)
diagram.addMaster(src, masterName)

# Adds shape with defined PinX and PinY.
diagram.addShape(2.0, 2.0, masterName, 0)
diagram.addShape(6.0, 6.0, masterName, 0)

diagram.save("AddMasterFromStencil_out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

