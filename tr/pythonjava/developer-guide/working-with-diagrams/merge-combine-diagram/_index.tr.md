---
title: Birleştir Birleştir Diagram
type: docs
weight: 30
url: /tr/python-java/merge-combine-diagram/
description: Bu bölümde visio dosyasının nasıl birleştirileceği açıklanmaktadır.
---
## **Olası Kullanım Senaryoları**

Python için Aspose.Diagram via Java, iki visio dosyasını bir dosyada birleştirmenizi sağlar.
Python via Java API için Aspose.Diagram, bir Visio çizimini temsil eden Diagram sınıfına sahiptir.
Yöntemi kullanma**birleştir** Diagram sınıfında diyagramları birleştirmek için.

## **Basit kod**
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

# Load another Visio diagram
diagram2 = Diagram("DrawingFlowChart.vsdx")

diagram2.combine(diagram)

# save in the VSDX format
diagram2.save("CombineDiagram_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
