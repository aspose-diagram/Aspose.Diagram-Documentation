---
title: Lägg till Master från Stencil
type: docs
weight: 30
url: /sv/python-java/add-master-from-stencil/
description: Det här avsnittet förklarar hur man lägger till master från stencil
---
## **Möjliga användningsscenarier**

 Aspose.Diagram för Python via Java låter dig lägga till master från stencil.
Aspose.Diagram för Python via Java API har Master class som representerar en Visio mall för ritningsform.
Använder metoden**addMaster** i Diagram klass för att lägga till master från stencil.

## **Exempelkod**
```
{{< highlight "python" >}}
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
```
