---
title: Alanları Kaldır
type: docs
weight: 20
url: /tr/python-java/remove-fields/
description: Bu bölümde alanların nasıl kaldırılacağı açıklanmaktadır.
---
## **Alanı Kaldır**
 Python via Java için Aspose.Diagram, Microsoft Office Otomasyon olmadan kendi uygulamalarınızdan Microsoft Visio diyagramlarına alan kaldırmanızı sağlar.

Field nesnesi, bir metin çalıştırmasındaki metin alanını temsil eder. Shape sınıfı tarafından sunulan field özelliği, Aspose.Diagram.Field nesnelerinin bir koleksiyonunu destekler.

### **Programlama Örneği**
Aşağıdaki kod parçası, şekildeki bir alanı kaldırır.

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load a Visio diagram
diagram = Diagram("InsertField_out.vsdx")

# Get page by name
page = diagram.getPages().getPage("Page-1")

# Get Visio Shape
shape = page.getShapes().get(0)

fld = shape.getFields().get(0)
# Remove field of shape
shape.getFields().remove(fld)

# Save diagram
diagram.save("RemoveField_out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}


