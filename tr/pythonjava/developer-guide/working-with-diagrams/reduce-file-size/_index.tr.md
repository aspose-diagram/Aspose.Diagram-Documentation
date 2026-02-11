---
title: Dosya Boyutunu Küçült
type: docs
weight: 50
url: /tr/python-java/reduce-file-size/
description: Bu bölüm, dosya boyutunu diagram'den Aspose.Diagram ile Python via Java için nasıl küçülteceğinizi açıklar.
---
## **Dosya Boyutunu Küçült**
 Python via Java API için Aspose.Diagram, geliştiricilerin dosya boyutunu azaltmak için bir diagram'den gizli bilgileri kaldırmasına olanak tanır.
 Sayfa nesnesi, bir ön plan sayfasının veya bir arka plan sayfasının çizim alanını temsil eder. Dosya boyutunu küçültmek için RemoveHiddenInfoItem özelliklerini**Gizli Bilgileri Kaldır()** Diagram sınıfının yöntemi. Aşağıdaki kod örneği, gizli bilgilerin diagram'den nasıl kaldırılacağını gösterir.

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

# Remove hidden information from diagram
diagram.removeHiddenInformation(RemoveHiddenInfoItem.SHAPES | RemoveHiddenInfoItem.MASTERS)

# save in the VSDX format
diagram.save("ReduceFileSize_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
