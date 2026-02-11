---
title: Aggiungi Master da Stencil
type: docs
weight: 30
url: /it/python-java/add-master-from-stencil/
description: Questa sezione spiega come aggiungere il master dallo stencil
---
## **Possibili scenari di utilizzo**

Aspose.Diagram for Python via Java allows you to add master from stencil. 
Aspose.Diagram for Python via Java API has the Master class that represents a Visio drawing shape template.
Usando il metodo**addMaster** nella classe Diagram per aggiungere master dallo stencil.

## **Codice di esempio**

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

