---
title:  Visio'i HTML biçimine dönüştür
linktitle: Visio'i HTML'e dönüştür
type: docs
weight: 30
url: /tr/python-java/convert-visio-to-html/
description: This topic show you how to convert Visio to html formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to html with a few lines of code.
---
## **Visio'i HTML'e aktar** ##
 Bu makalede, bir Microsoft Visio diagram'in HTML kullanılarak nasıl dışa aktarılacağı açıklanmaktadır.[Python via Java için Aspose.Diagram](https://products.aspose.com/diagram/python-java/) API.

diagram dosyalarını okumak için Diagram sınıf oluşturucusunu ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemini kullanın. Geliştiriciler, ortaya çıkan HTML'i yerel depolamaya veya doğrudan bir akış örneğine kaydedebilir.

 Aşağıdaki resimde bir[VSD dosya](ExportToHTML.vsd)PNG formatında kaydedilmek üzere. Diğer diagram formatlarını da (VSDX, VSTM, VSTM, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, 07611071) kullanabilirsiniz.

**diagram'i girin.**

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/YX4BNNq.png)

VSD diagram'i HTML'e aktarmak için aşağıdaki adımları gerçekleştirin:

1. Diagram sınıfının bir örneğini oluşturun.
1. Dagram sınıfının Save yöntemini çağırın ve çıktı formatı olarak HTML'i ayarlayın.

Aşağıdaki görüntü HTML çıktı dosyasını göstermektedir.

**Çıkış HTML diagram.**

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/syavUqI.png)

### **Ortaya çıkan HTML'i yerel depoya kaydedin**
Ortaya çıkan dosya, dosya adı ve uzantısı dahil olmak üzere tam bir yol dizesi iletilerek kaydedilebilir, örneğin @"c:\temp\MyOutput.html".

#### **Sonuç HTML'i Yerel Depolama Programlama Örneğine Kaydet**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToHTML.py" >}}



### **Elde edilen HTML'i bir akış örneğine kaydedin**
Elde edilen HTML'i yerel depoda saklamadan bir veritabanına veya havuza kaydetmek kullanım durumu içindir. Bu özellik aynı zamanda HTML'in diğer sonuç kaynaklarını, örneğin yazı tiplerini, CSS'yi (stil bilgilerini içeren) ve resimleri de içerir. Akış örneğine tek bir HTML dosyası kaydettiği için.
#### **Sonuç HTML'i Akış Programlama Örneğine Kaydet**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportHTMLinStream.py" >}}
