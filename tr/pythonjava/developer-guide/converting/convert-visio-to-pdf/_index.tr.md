---
title:  Visio'i PDF biçimine dönüştür
linktitle: Visio'i PDF'e dönüştür
type: docs
weight: 10
url: /tr/python-java/convert-visio-to-pdf/
description: This topic show you how to convert Visio to PDF formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to PDF with a few lines of code.
---
## **PDF'e aktarılıyor**
{{% alert color="primary" %}}

Python için Aspose.Diagram via Java API ve Sürüm Numarası ile ilgili bilgileri doğrudan çıktı belgelerine yazar. Örneğin, PDF'e bir Çizim oluşturulduğunda, Aspose.Diagram for Java doldurulur**Başvuru**'Aspose.Diagram' değerine sahip alan ve**PDF Yapımcı**değeri olan alan, örneğin 'Aspose.Diagram 17.9'.

Python via Java için Aspose.Diagram'e bu bilgileri çıktı Belgelerinden değiştirme veya kaldırma talimatı veremeyeceğinizi lütfen unutmayın.

{{% /alert %}}

Bu makalede, Python via Java için Aspose.Diagram kullanılarak bir Microsoft Visio diagram'in PDF'e nasıl aktarılacağı açıklanmaktadır.

diagram dosyalarını okumak için Diagram sınıfının yapıcısını ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemini kullanın.

[VSD diagram](ExportToPDF.vsd)PDF'i dışa aktarmak için örnek çizim dosyasıdır. Diğer diagram formatlarını (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, 076137481 veya 40.1937610) kullanabilirsiniz.

VSD diagram'i PDF'e dışa aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Diagram sınıfı Save yöntemini çağırın ve çıktı formatını PDF olarak ayarlayın.

### **PDF Programlama Örneğine Aktarma**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSD file
diagram = Diagram("ExportToPDF.vsd")

# Save as PDF file format
diagram.save("ExportToPDF_Out.pdf", SaveFileFormat.PDF)

jpype.shutdownJVM()

{{< /highlight >}}
```

### **Birden Çok Sayfayı Böl**
Aspose.Diagram for Java, Microsoft Visio Diagram'i PDF'e dönüştürürken birden fazla sayfanın bölünmesine izin verir. Aşağıdaki kod parçacığı işlevselliği gösterir.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSDX file
diagram = Diagram("Network Diagram_start.vsdx")
# Options when saving a diagram into the PDF format
options = PdfSaveOptions()
# set SplitMultiPages option
options.setSplitMultiPages(True)
# save in PDF format
diagram.save("SplitMultiPages.pdf", options)

jpype.shutdownJVM()

{{< /highlight >}}
```
