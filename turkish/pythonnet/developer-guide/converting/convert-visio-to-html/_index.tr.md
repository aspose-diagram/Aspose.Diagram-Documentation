---
title:  Visio'i HTML biçimine dönüştür
linktitle: Visio'i HTML'ye dönüştür
type: docs
weight: 30
url: /tr/python-net/convert-visio-to-html/
description: Bu konu, Aspose.Diagram'in Visio'i html biçimlerine dönüştürmeye nasıl izin verdiğini gösterir. VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM'i birkaç satır kodla html'ye dönüştürün.
---
## **Visio'i HTML'ye aktar**
 Bu makalede, bir Microsoft Visio diagram'in kullanılarak HTML'ye nasıl aktarılacağı açıklanmaktadır.[.NET üzerinden Python için Aspose.Diagram](https://products.aspose.com/diagram/python-net/) API.

diagram dosyalarını okumak için Diagram sınıf oluşturucusunu ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemini kullanın. Geliştiriciler, ortaya çıkan HTML'yi yerel depolamaya veya doğrudan bir akış örneğine kaydedebilir.

1. [Ortaya çıkan HTML'yi yerel depolamaya kaydedin](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-the-local-storage).
1. [Elde edilen HTML'yi bir akış örneğine kaydedin](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-a-stream-instance).

Aşağıdaki resimde, PNG formatında kaydedilmek üzere olan bir VSD dosyası gösterilmektedir. Diğer diagram formatlarını da (VSDX, VSDM, VSTX, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, VTX1 veya 3.761) kullanabilirsiniz.

|**diagram'i girin.**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](how-to-convert-a-visio-diagram_6.png)|
VSD diagram'i HTML'ye aktarmak için aşağıdaki adımları gerçekleştirin:

1. Diagram sınıfının bir örneğini oluşturun.
1. Dagram sınıfının Save yöntemini çağırın ve çıktı formatı olarak HTML'yi ayarlayın.
### **Ortaya çıkan HTML'yi yerel depolamaya kaydedin**
Ortaya çıkan dosya, dosya adı ve uzantısı dahil olmak üzere tam bir yol dizesi iletilerek kaydedilebilir, örneğin @"c:\temp\MyOutput.html".
#### **Sonuç HTML'sini Yerel Depolama Programlama Örneğine Kaydet**
{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToHTML.py" >}}
