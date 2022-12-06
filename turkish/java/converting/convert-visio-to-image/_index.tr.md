---
title:  Visio'i Görüntü biçimlerine dönüştür
linktitle: Visio'i Görsellere Dönüştür
type: docs
weight: 20
url: /tr/java/convert-visio-to-image/
description: Bu konuda, Aspose.Diagram'in Visio'i çeşitli resim formatlarına nasıl dönüştürebileceğiniz gösterilmektedir. Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM görüntülerini birkaç satır kodla PNG, JPEG, BMP'ye dönüştürün.
---
## **Diyagramları Görüntü Dosyası Formatlarına Aktarma**
 Bu makalede, Microsoft Visio diagram'in kullanılarak bir görüntüye nasıl aktarılacağı açıklanmaktadır.[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Kullan[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)diagram dosyalarını okumak için 'class' yapıcısı ve diagram'i desteklenen herhangi bir görüntü biçimine dışa aktarmak için Kaydet yöntemi. Aşağıdaki görüntü, PNG biçimine kaydedilmek üzere olan bir VSD dosyasını göstermektedir. Diğer diagram formatlarını da (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX veya VSX) kullanabilirsiniz.
**Kaynak dosya. Ok ve Üçgen etiketlerinin kalın yazıldığına dikkat edin.**

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/WOV36ek.png)

diagram'i bir görüntüye dışa aktarmak için:

- Diagram sınıfının bir örneğini oluşturun.
- Diagram sınıfının Save yöntemini çağırın ve dışa aktarmak istediğiniz görüntü formatını ayarlayın. Çıktı görüntü dosyası orijinal dosyaya benziyor.

**Çıktı PNG dosyası.**

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/WOV36ek.png)
### **Görüntü Dosyası Programlama Örneğine Aktarma**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToImage-ExportToImage.java" >}}

Belgenin tamamı yerine belirli bir sayfayı resme kaydetmek de mümkündür:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportPageToImage-ExportPageToImage.java" >}}