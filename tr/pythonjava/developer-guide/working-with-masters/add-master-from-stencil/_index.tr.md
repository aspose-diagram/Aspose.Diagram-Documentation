---
title: Stencil'den Master Ekle
type: docs
weight: 30
url: /tr/python-java/add-master-from-stencil/
description: Bu bölüm şablondan nasıl master ekleneceğini açıklar
---
## **Olası Kullanım Senaryoları**

 Python için Aspose.Diagram via Java şablondan master eklemenizi sağlar.
Python via Java API için Aspose.Diagram, bir Visio çizim şekli şablonunu temsil eden Master sınıfına sahiptir.
Yöntemi kullanma**ek usta** şablondan master eklemek için Diagram sınıfında.

## **Basit kod**
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
