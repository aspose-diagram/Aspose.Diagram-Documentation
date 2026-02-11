---
title: Alanları Güncelle
type: docs
weight: 20
url: /tr/python-java/update-fields/
description: Bu bölümde alanların nasıl güncelleneceği açıklanmaktadır.
---
## **Alanı Güncelle**
Python via Java için Aspose.Diagram, Microsoft Office Otomasyonu olmadan kendi uygulamalarınızdan alanı Microsoft Visio diyagramlarına güncellemenizi sağlar.

Field nesnesi, bir metin çalıştırmasındaki metin alanını temsil eder. Shape sınıfı tarafından sunulan field özelliği, Aspose.Diagram.Field nesnelerinin bir koleksiyonunu destekler.

### **Programlama Örneği**
Aşağıdaki kod parçası, şekildeki bir alanı günceller.
```
{{< highlight "python" >}}
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
# Update format of field
fld.getFormat().setVal("")
fld.getFormat().getUfev().setUnit(MeasureConst.UNDEFINED)
fld.getFormat().getUfev().setF("")

# Update value of field
fld.getValue().setVal("1")
fld.getValue().getUfev().setF("")
fld.getValue().getUfev().setUnit(MeasureConst.UNDEFINED)

# Save diagram 
diagram.save("UpdateField_out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
