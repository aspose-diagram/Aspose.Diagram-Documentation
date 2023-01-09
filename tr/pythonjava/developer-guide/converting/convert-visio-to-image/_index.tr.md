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
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToImage.py" >}}

Belgenin tamamı yerine belirli bir sayfayı resme kaydetmek de mümkündür:

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportPageToImage.py" >}}