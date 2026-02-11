---
title: Yorumlarla Çalışmak
type: docs
weight: 210
url: /tr/python-java/working-with-comments/
description: Bu sayfa, Visio çiziminin bir sayfasına Aspose.Diagram kitaplığı ile nasıl yorum ekleneceğini açıklar.
---
## **Visio'de Sayfa Düzeyinde Yorum ekleyin**
 Python via Java API için Aspose.Diagram, geliştiricilerin bir sayfada herhangi bir yere yorum eklemesine olanak tanır[Visio çizimi](DrawingComment.vsdx).
### **Yorum ekle**
Page sınıfı tarafından sunulan addComment yöntemi, bir çizim sayfasına yorum eklemenize olanak tanır. Bir yorum dizesiyle birlikte X ve Y koordinatlarını alır.

Microsoft Visio kullanıcıları, sayfanın sol üst köşesinde bir simge ile sunulan tüm sayfaya yorum ekler. Geliştiriciler Visio'de sayfa düzeyinde yorumlar ekleyebilir. Python için Aspose.Diagram via Java API ayrıca Visio'de sayfa düzeyinde açıklamayı değiştirmeyi destekler.
#### **Sayfa Düzeyinde Yorum Programlama Örneği Ekle**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram
diagram = Diagram("DrawingComment.vsdx")

# Add comment
diagram.getPages().getPage(0).addComment(7.205905511811023, 3.880708661417323, "test@")

# Save diagram
diagram.save("AddPageLevelCommentInVisio_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
## **Visio Diagram'de bir Sayfa Düzeyinde Yorum düzenleyin**
Python için Aspose.Diagram via Java API, sayfa düzeyinde yorumu değiştirme desteğine sahiptir[Visio çizimi](DrawingComment.vsdx) sayfanın sol üst köşesinde bir simgeyle gösterilen sayfa.
### **Yorumu Düzenle**
Annotation sınıfı tarafından sunulan Comment özelliği, geliştiricilerin Visio çizim sayfasındaki yorumları düzenlemesine olanak tanır.
#### **Yorum Programlama Örneği Düzenle**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load Visio
diagram = Diagram("DrawingComment.vsdx")

# get collection of the annotations
annotations = diagram.getPages().getPage("Page-1").getPageSheet().getAnnotations()

# iterate through the annotations
for annotation in annotations:
    comment = annotation.getComment().getValue()
    comment += "Updation mark"
    annotation.getComment().setValue(comment)

# save Visio
diagram.save("EditPageLevelCommentInVisio_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
## **Visio Çiziminde Şekil Düzeyinde Yorum Ekleme**
 Python via Java API için Aspose.Diagram geliştiricilerin şekle yorum eklemesine izin verir.[Visio çizimi](DrawingComment.vsdx).
### **Yorum ekle**
Page sınıfı tarafından sunulan aşırı yüklenmiş bir addComment yöntemi, bir Shape sınıfı örneğini ve yorumun metin dizesini alır.
#### **Şekil Düzeyinde Yorum Programlama Örneği Ekleme**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load diagram
diagram = Diagram("DrawingComment.vsdx")

# retrieve page by name
page = diagram.getPages().getPage("Page-1")

# retrieve shape by ID
shape = page.getShapes().getShape(1)

page.addComment(shape, "Hello")

# save diagram
diagram.save("AddShapeLevelCommentInVisio_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
