---
title:  Visio'i Görüntü biçimlerine dönüştür
linktitle: Visio'i Görsellere Dönüştür
type: docs
weight: 20
url: /tr/python-java/convert-visio-to-image/
description: This topic show you how to convert Visio to various images formats using Aspose.Diagram for Python via Java. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to PNG, JPEG, BMP images with a birkaç kod satırı.
---
## **Diyagramları Görüntü Dosyası Formatlarına Aktarma**
Bu makalede, Python via Java için Aspose.Diagram kullanılarak bir Microsoft Visio diagram'in bir görüntüye nasıl aktarılacağı açıklanmaktadır.

diagram dosyalarını okumak için Diagram sınıfının yapıcısını ve diagram'i desteklenen herhangi bir resim formatına dışa aktarmak için Save yöntemini kullanın. Aşağıdaki resim, PNG formatında kaydedilmek üzere olan bir VSD dosyasını göstermektedir. Diğer diagram formatlarını da (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX veya VSX) kullanabilirsiniz.

**[Örnek VSD dosyası.](ExportToImage.vsd)**

diagram'i bir görüntüye dışa aktarmak için:

- Diagram sınıfının bir örneğini oluşturun.
- Diagram sınıfının Save yöntemini çağırın ve dışa aktarmak istediğiniz görüntü formatını ayarlayın. Çıktı görüntü dosyası orijinal dosyaya benziyor.

**Çıktı PNG dosyası.**

![yapılacaklar:resim_alternatif_Metin](ExportToImage.png)
### **Görüntü Dosyası Programlama Örneğine Aktarma**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSD file
diagram = Diagram("ExportToImage.vsd")

# Save as PNG
diagram.save("ExportToImage_Out.png", SaveFileFormat.PNG)

jpype.shutdownJVM()

{{< /highlight >}}
```

Belgenin tamamı yerine belirli bir sayfayı resme kaydetmek de mümkündür:

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load diagram
diagram = Diagram("ExportToImage.vsd")

# Save diagram as PNG
options = ImageSaveOptions(SaveFileFormat.PNG)

# Save one page only, by page index
options.setPageIndex(0)

# Save resultant Image file
diagram.save("ExportPageToImage_Out.png", options)

jpype.shutdownJVM()

{{< /highlight >}}
```