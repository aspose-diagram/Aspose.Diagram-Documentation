---
title:  Visio'i HTML biçimine dönüştür
linktitle: Visio'i HTML'ye dönüştür
type: docs
weight: 30
url: /tr/python-java/convert-visio-to-html/
description: Bu konu size 07613481 için Aspose.Diagram kullanılarak Visio'i HTML formatlarına nasıl dönüştüreceğinizi gösterir. 07613481 üzerinden 07613481 için.
---
## **Visio'i HTML'ye aktar** ##
 Bu makalede, bir Microsoft Visio diagram'in kullanılarak HTML'ye nasıl aktarılacağı açıklanmaktadır.[Java üzerinden Python için Aspose.Diagram](https://products.aspose.com/diagram/python-java/) API.

diagram dosyalarını okumak için Diagram sınıf oluşturucusunu ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemini kullanın. Geliştiriciler, ortaya çıkan HTML'yi yerel depolamaya veya doğrudan bir akış örneğine kaydedebilir.

 Aşağıdaki resimde bir[VSD dosya](ExportToHTML.vsd)PNG formatında kaydedilmek üzere. Diğer diagram formatlarını da kullanabilirsiniz (VSDX, VSTM, VSTM, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, VTX veya 307611)

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
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToHTML.py" >}}



### **Elde edilen HTML'yi bir akış örneğine kaydedin**
Ortaya çıkan HTML'yi yerel depoda saklamadan bir veritabanına veya havuza kaydetmek kullanım durumu içindir. Bu özellik aynı zamanda HTML'nin diğer sonuç kaynaklarını, örneğin yazı tiplerini, CSS'yi (stil bilgilerini içeren) ve resimleri de gömer. Akış örneğine tek bir HTML dosyası kaydettiği için.
#### **Sonuç HTML'sini Akış Programlama Örneğine Kaydetme**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportHTMLinStream.py" >}}
