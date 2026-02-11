---
title: Oluştur, Alan ekle
type: docs
weight: 10
url: /tr/python-java/create-insert-fields/
description: Java Diagram API kullanarak alanlar nasıl oluşturulur, eklenir.
---
## **Alan ekle**
 Python via Java için Aspose.Diagram, Microsoft Office Otomasyonu olmadan kendi uygulamalarınızdan Microsoft Visio diyagramlarına alan oluşturmanıza ve eklemenize olanak tanır.

### **Programlama Örneği**
Aşağıdaki kod parçası, şekle bir alan ekler.

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load a Visio diagram
diagram = Diagram("Drawing1.vsdx")

# Get page by name
page = diagram.getPages().getPage("Page-1")

# Get Visio Shape
shape = page.getShapes().get(0)
# Insert field
fld = Field()
fld.getValue().setVal("1")
shape.getFields().add(fld)

# Save diagram 
diagram.save("InsertField_out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}


