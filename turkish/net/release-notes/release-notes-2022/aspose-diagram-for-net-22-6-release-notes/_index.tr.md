---
title: Aspose.Diagram for .NET 22.6 Sürüm Notları
type: docs
weight: 22
url: /tr/net/aspose-diagram-for-net-22-6-release-notes/
---
{{% alert color="primary" %}} 

Bu sayfa Aspose.Diagram for .NET 22.6 için sürüm notları bilgilerini içerir.

{{% /alert %}} 
## **İyileştirmeler ve Değişiklikler**

|**Anahtar**|**Özet**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-52826|VSDM'i PDF'ye kaydederken bağlantı koptu|Artırma|
|DIAGRAMNET-52851|Bazı şekiller svg'ye dönüştürüldükten sonra eğrilerini kaybediyor|Artırma|
|DIAGRAMNET-52858|HTML'de görüntü kalitesi|Artırma|
|DIAGRAMNET-52825|HTML sorununa aktar|Böcek|
|DIAGRAMNET-52832|Visio'den PDF/SVG'ye - Döndürülen metin konumu değiştirildi|Böcek|
|DIAGRAMNET-52840|HTML önizlemesindeki öğeler bulanıklaştırıldı|Böcek|
|DIAGRAMNET-52842|Sayfayı otomatik sığdır, otomatik olarak sığdırmaz|Böcek|
|DIAGRAMNET-52849|Dönüştürmeden sonra küçültülmemiş raster görüntüler|Böcek|
|DIAGRAMNET-52852|VSD Açma Hatası - Aspose.Diagram.DiagramException|Böcek|

## **Herkese Açık API ve Geriye Dönük Uyumsuz Değişiklikler**
Aşağıda, API numaralı telefon numarasına eklenen, yeniden adlandırılan, kaldırılan veya kullanımdan kaldırılan üyeler gibi genele açık olarak yapılan tüm değişikliklerin ve Aspose.Diagram for .NET numaralı telefona yapılan geriye dönük uyumlu olmayan değişikliklerin bir listesi bulunmaktadır. Listelenen herhangi bir değişiklikle ilgili endişeleriniz varsa lütfen şu adrese bildirin: Aspose.Diagram destek forumu.
### **HTMLSaveOptions'a Çözünürlük Ekler**
- Oluşturulan html'nin çözünürlüğünü inç başına nokta cinsinden alır veya ayarlar.

{{< highlight "java" >}}
HTMLSaveOptions option = new HTMLSaveOptions();
option.Resolution = 96;
{{< /highlight >}}
