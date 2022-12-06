---
title: Aspose.Diagram for .NET 19.4 Sürüm Notları
type: docs
weight: 90
url: /tr/net/aspose-diagram-for-net-19-4-release-notes/
---
{{% alert color="primary" %}} 

Bu sayfa için sürüm notları içerir[Aspose.Diagram for .NET 19.4](https://www.nuget.org/packages/Aspose.Diagram/19.4.0)

{{% /alert %}} 
## **İyileştirmeler ve Değişiklikler**

|**Anahtar**|**Özet**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51602|Gömülü XSLX nesnesi, manipülasyondan sonra bozuluyor|Artırma|
|DIAGRAMNET-51625|.vsdx dosyalarındaki harici excel verileri, Diagram yeniden kaydedildiğinde kaldırılır|Artırma|
|DIAGRAMNET-51626|API excel verilerini işlemez|Artırma|
|DIAGRAMNET-51627|Dependson formülü temelinde şekil verilerini ayıklayın|Artırma|
|DIAGRAMNET-51629|Bir çizimi sığdırmak için bir sayfayı büyütmek işe yaramıyor gibi görünüyor|Artırma|
|DIAGRAMNET-51176|Bir VSDM, SVG'ye dönüştürülürken degrade başlık çubuğu değiştirilir|Böcek|
|DIAGRAMNET-51404|VSD - Resim - Şekil rengi koyu|Böcek|
|DIAGRAMNET-51473|VDX'den PDF'ye - Yanlış arka plan rengi|Böcek|
|DIAGRAMNET-51475|VSDX'den PDF'ye - Degradeler tersine işleniyor|Böcek|
|DIAGRAMNET-51616|Visio'den PDF'ye - Degrade, çıktı PDF'sinde baş aşağı işleniyor|Böcek|
|DIAGRAMNET-51630|VSDX'den HTML'ye - Şekillerin arka plan rengi çıktıda mevcut değil|Böcek|
|DIAGRAMNET-51631|VSDX'den PDF'ye - Şekillerin arka plan rengi çıktıda mevcut değil|Böcek|
|DIAGRAMNET-51632|VSD'den SVG'ye - '' türündeki nesne " " türüne aktarılamadı İstisna oluştu|Böcek|

## **Herkese Açık API ve Geriye Dönük Uyumsuz Değişiklikler**
Aşağıda, API numaralı telefon numarasına eklenen, yeniden adlandırılan, kaldırılan veya kullanımdan kaldırılan üyeler gibi genele açık olarak yapılan değişikliklerin ve Aspose.Diagram for .NET numaralı telefona yapılan geriye dönük uyumlu olmayan değişikliklerin bir listesi bulunmaktadır. Listelenen herhangi bir değişiklikle ilgili endişeleriniz varsa lütfen the[Aspose.Diagram destek forumu](https://forum.aspose.com/c/diagram/17).
### **Enum RemoveHiddenInfoItem ekler**
diagram için gizli bilgileri kaldırmayı belirtir.
### **Diagram'de RemoveHiddenInfoItem ekler**
Kullanılmayan bilgileri kaldırın.

{{< highlight "java" >}}

diagram.RemoveHiddenInformation((int)(RemoveHiddenInfoItem.Shapes | RemoveHiddenInfoItem.Masters));

{{< /highlight >}}
