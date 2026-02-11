---
title:  Visio'i HTML biçimine dönüştür
linktitle: Visio'i HTML'e dönüştür
type: docs
weight: 30
url: /tr/python-net/convert-visio-to-html/
description: Bu konu, Aspose.Diagram'in Visio'i html biçimlerine dönüştürmeye nasıl izin verdiğini gösterir. VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM'i birkaç satır kodla html'ye dönüştürün.
---
## **Visio'i HTML'e aktar**
 Bu makalede, bir Microsoft Visio diagram'in HTML kullanılarak nasıl dışa aktarılacağı açıklanmaktadır.[Python via .NET için Aspose.Diagram](https://products.aspose.com/diagram/python-net/) API.

diagram dosyalarını okumak için Diagram sınıf oluşturucusunu ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemini kullanın. Geliştiriciler, ortaya çıkan HTML'i yerel depolamaya veya doğrudan bir akış örneğine kaydedebilir.

1. [Ortaya çıkan HTML'i yerel depoya kaydedin](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-the-local-storage).
1. [Elde edilen HTML'i bir akış örneğine kaydedin](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-a-stream-instance).

Aşağıdaki resimde, PNG biçiminde kaydedilmek üzere olan bir VSD dosyası gösterilmektedir. Diğer diagram formatlarını da kullanabilirsiniz (VSDX, VSDM, VSTX, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, 04811203)

|**diagram'i girin.**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](how-to-convert-a-visio-diagram_6.png)|
VSD diagram'i HTML'e aktarmak için aşağıdaki adımları gerçekleştirin:

1. Diagram sınıfının bir örneğini oluşturun.
1. Dagram sınıfının Save yöntemini çağırın ve çıktı formatı olarak HTML'i ayarlayın.
### **Ortaya çıkan HTML'i yerel depoya kaydedin**
Ortaya çıkan dosya, dosya adı ve uzantısı dahil olmak üzere tam bir yol dizesi iletilerek kaydedilebilir, örneğin @"c:\temp\MyOutput.html".
#### **Sonuç HTML'i Yerel Depolama Programlama Örneğine Kaydet**

{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the html format
diagram.save("Visio_out.html", SaveFileFormat.HTML)
{{< /highlight >}}

