---
title: Görüntülerle Çalışmak
type: docs
weight: 70
url: /tr/python-java/working-with-images/
description: Bu sayfa, Visio çiziminin bir sayfasından Aspose.Diagram kitaplığıyla bir görüntünün nasıl çıkarılacağını, değiştirileceğini veya ekleneceğini açıklar.
---
## **Visio Sayfasından Tüm Resimleri Çıkarın**
 Microsoft Visio'de sayfalar ya ön plan ya da arka plan sayfalarıdır. Belirli bir sayfadan görüntüleri ayıklayabilirsiniz.[Visio dosyası](ExtractAllImagesFromPage.vsd).
### **Görüntüleri Çıkar**
Sayfa Sınıfı nesnesi, bir ön plan sayfasının veya bir arka plan sayfasının çizim alanını temsil eder. Diagram sınıfı tarafından sunulan Shapes özelliği, Aspose.Diagram.Shape nesnelerinin bir koleksiyonunu destekler. Bu özellik, belirli bir sayfadaki tüm görüntüleri çıkarmak için kullanılabilir.
#### **Görüntüleri Çıkarma Programlama Örneği**
Aşağıdaki kod parçası, belirli bir Visio sayfasından tüm resimleri çıkarır.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# call a Diagram class constructor to load a VSD diagram
diagram = Diagram("ExtractAllImagesFromPage.vsd")

# Enter page index i.e. 0 for first one
for shape in diagram.getPages().getPage(0).getShapes():
    # Filter shapes by type Foreign
    if shape.getType() == TypeValue.FOREIGN:
        fos = java.io.FileOutputStream("ExtractAllImages" + str(shape.getID()) + "_Out.bmp")
        fos.write(shape.getForeignData().getValue())
        fos.close()

jpype.shutdownJVM()

{{< /highlight >}}
```
## **Çeşitli Visio Şekillerinin Simgelerini Alın**
 Python via Java API için Aspose.Diagram artık geliştiricilerin çeşitli simgeleri almasına izin veriyor[Visio şekiller](Timeline.vss). 
### **Şekil Simgesini Alma**
Aşağıdaki örneklerdeki kod, nasıl yapılacağını gösterir:

1. Mevcut bir diagram veya şablonu yükleyin.
1. Ana dizine göre alın
1. Ana simgeyi alın.
1. Simgeyi yerel alana kaydedin.
#### **Simge Programlama Örneği Alın**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Load stencil file to a diagram object
stencil = Diagram("Timeline.vss")
# get master
master = stencil.getMasters().getMasterByName("Triangle milestone")
# get byte array
icon_bytes = master.getIcon()
# create an image file
fos = java.io.FileOutputStream("MasterIcon_Out.png")
# write byte array of the image
fos.write(icon_bytes)
# close array
fos.close()
jpype.shutdownJVM()

{{< /highlight >}}
```
## **Visio Diagram'in Resim Şeklini Değiştirme**
 Python via Java API için Aspose.Diagram, geliştiricilerin mevcut resim şekillerine erişmesine ve bunları değiştirmesine olanak tanır.[Visio diagram](ExtractAllImagesFromPage.vsd).
### **Resim Şeklini Değiştirme**
Aşağıdaki örneklerdeki kod, nasıl yapılacağını gösterir:

1. Mevcut bir diagram yükleyin.
1. Seçici sayfa şekillerini yineleyin.
1. Resim şekilleri elde etmek için filtre uygulayın.
1. Ortaya çıkan Visio diagram'i yerel alana kaydedin.
#### **Bir Resim Şekli Programlama Örneğinin Değiştirilmesi**
```
{{< highlight "python" >}}
import jpype
import asposediagram

jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# call a Diagram class constructor to load the VSD diagram
diagram = Diagram("ExtractAllImagesFromPage.vsd")

# convert image into bytes array       
fi = java.io.File("image.png")
fileContent = java.nio.file.Files.readAllBytes(fi.toPath())

# Enter page index i.e. 0 for first one
for shape in diagram.getPages().getPage(0).getShapes():
    # Filter shapes by type Foreign
    if shape.getType() == TypeValue.FOREIGN:
        # replace picture shape
        shape.getForeignData().setValue(fileContent)

# save diagram
diagram.save("ReplaceShapePicture_Out.vsdx", SaveFileFormat.VSDX)
jpype.shutdownJVM()

{{< /highlight >}}
```
## **Görüntüyü Visio Şekli Olarak İçe Aktar**
Python via Java API için Aspose.Diagram artık geliştiricilerin bir görüntüyü Microsoft Visio şekli olarak içe aktarmasına izin veriyor.
### **Visio'e bir Resim ekleyin**
Aşağıdaki örneklerdeki kod, nasıl yapılacağını gösterir:

1. Bir diagram oluşturun.
1. Visio sayfasını edinin
1. Bir görüntüyü Visio şekli olarak içe aktarın
1. diagram'i kaydedin.
#### **Görüntü Programlama Örneği Ekleme**
```
{{< highlight "python" >}}
import jpype
import asposediagram

jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Create a new diagram
diagram = Diagram()

# Get page object by index
page0 = diagram.getPages().getPage(0)
# Set pinX, pinY, width and height
pinX = 2
pinY = 2
width = 4
height = 3

# Import Bitmap image as Visio shape
page0.addShape(pinX, pinY, width, height, java.io.FileInputStream("image.png"))

# Save Visio diagram
diagram.save("InsertImageInVisio_out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
