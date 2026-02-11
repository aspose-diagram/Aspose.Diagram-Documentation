---
title: Добавить мастер из трафарета
type: docs
weight: 30
url: /ru/python-java/add-master-from-stencil/
description: В этом разделе объясняется, как добавить мастер из трафарета
---
## **Возможные сценарии использования**

 Aspose.Diagram для Python via Java позволяет добавить мастер из трафарета.
Aspose.Diagram для Python via Java API содержит мастер-класс, представляющий шаблон формы чертежа Visio.
Использование метода**аддмастер** в классе Diagram добавить мастера из трафарета.

## **Образец кода**

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

