---
title:  Visio'i HTML biçimine dönüştür
linktitle: Visio'i HTML'ye dönüştür
type: docs
weight: 30
url: /tr/java/convert-visio-to-html/
description: Bu konu, Aspose.Diagram'in Visio'i html biçimlerine dönüştürmeye nasıl izin verdiğini gösterir. VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM'i birkaç satır kodla html'ye dönüştürün.
---
## **Visio'i HTML'ye aktar** **Visio'i HTML'ye aktar**
 Bu makalede, bir Microsoft Visio diagram'in kullanılarak HTML'ye nasıl aktarılacağı açıklanmaktadır.[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Kullan[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) diagram dosyalarını okumak için sınıf yapıcısı ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemi. Geliştiriciler, ortaya çıkan HTML'yi yerel depolamaya veya doğrudan bir akış örneğine kaydedebilir.

1. [Ortaya çıkan HTML'yi yerel depolamaya kaydedin](/diagram/tr/java/how-to-convert-a-visio-diagram/).
1. [Elde edilen HTML'yi bir akış örneğine kaydedin](/diagram/tr/java/how-to-convert-a-visio-diagram/).

Aşağıdaki resimde, PNG formatında kaydedilmek üzere olan bir VSD dosyası gösterilmektedir. Diğer diagram formatlarını da (VSDX, VSTM, VSTM, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, VTX1 veya 3.761) kullanabilirsiniz.

**diagram'i girin.**

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/YX4BNNq.png)

VSD diagram'i HTML'ye aktarmak için aşağıdaki adımları gerçekleştirin:

1. Diagram sınıfının bir örneğini oluşturun.
1. Dagram sınıfının Save yöntemini çağırın ve çıktı formatı olarak HTML'yi ayarlayın.

Aşağıdaki resim çıktı HTML dosyasını göstermektedir.

**Çıkış HTML'si diagram.**

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/syavUqI.png)
### **Ortaya çıkan HTML'yi yerel depolamaya kaydedin**
Ortaya çıkan dosya, dosya adı ve uzantısı dahil olmak üzere tam bir yol dizesi iletilerek kaydedilebilir, örneğin @"c:\temp\MyOutput.html".
#### **Sonuç HTML'sini Yerel Depolama Programlama Örneğine Kaydet**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToHTML-ExportToHTML.java" >}}



### **Elde edilen HTML'yi bir akış örneğine kaydedin**
Ortaya çıkan HTML'yi yerel depoda saklamadan bir veritabanına veya havuza kaydetmek kullanım durumu içindir. Bu özellik aynı zamanda HTML'nin diğer sonuç kaynaklarını, örneğin yazı tiplerini, CSS'yi (stil bilgilerini içeren) ve resimleri de gömer. Akış örneğine tek bir HTML dosyası kaydettiği için.
#### **Sonuç HTML'sini Akış Programlama Örneğine Kaydetme**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportHTMLinStream-ExportHTMLinStream.java" >}}
