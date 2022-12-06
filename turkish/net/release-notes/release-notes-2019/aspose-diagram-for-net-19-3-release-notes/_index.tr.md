---
title: Aspose.Diagram for .NET 19.3 Sürüm Notları
type: docs
weight: 100
url: /tr/net/aspose-diagram-for-net-19-3-release-notes/
---
{{% alert color="primary" %}} 

Bu sayfa için sürüm notları içerir[Aspose.Diagram for .NET 19.3](https://www.nuget.org/packages/Aspose.Diagram/19.3.0)

{{% /alert %}} 
## **İyileştirmeler ve Değişiklikler**

|**Anahtar**|**Özet**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-50930|İşletim sistemlerinde ortak yazı tipi dizinlerini alma desteği ekleyin|Artırma|
|DIAGRAMNET-51614|Bir Şekil için tüm Donanım değerlerini al|Artırma|
|DIAGRAMNET-50214|VSD'den PDF'e dönüştürme - Eğri çizgiler düz bir çizgiye dönüşür|Böcek|
|DIAGRAMNET-50240|VSD'den PDF'e dönüştürme - Dinamik bağlayıcıların yanlış düzeni|Böcek|
|DIAGRAMNET-50703|VSDX'den PDF'e dışa aktarma - Eksik bir dinamik bağlayıcı|Böcek|
|DIAGRAMNET-50704|VSD'den PDF'e dışa aktarma - Meta tipi şekiller dağınık sembollere dönüşüyor|Böcek|
|DIAGRAMNET-51535|VSDM'den SVG'ye - Yazı tipi, SVG'de Sans'tan Serif'e değişir|Böcek|
|DIAGRAMNET-51574|VSDX'den PNG'ye - PNG çıktısında bazı şekiller yanlış işleniyor|Böcek|
|DIAGRAMNET-51608|Metin Kaydırma beklendiği gibi çalışmıyor|Böcek|
|DIAGRAMNET-51609|Diagram, PowerPoint Slide'a kopyalandığında şekiller sola kaydırılıyor|Böcek|
|DIAGRAMNET-51617|Visio'den PDF'ye - Harici Veriye Dayalı değerler doğru şekilde gösterilmiyor|Böcek|
|DIAGRAMNET-51619|Visio - PDF - PDF'de Yanlış Tarih/Saat/Mesafe|Böcek|
|DIAGRAMNET-51621|Visio'den PDF'e - Arka plan görüntüsü bozuk ve PDF'de fazladan sayfa var|Böcek|
## **Herkese Açık API ve Geriye Dönük Uyumsuz Değişiklikler**
Aşağıda, API numaralı telefon numarasına eklenen, yeniden adlandırılan, kaldırılan veya kullanımdan kaldırılan üyeler gibi genele açık olarak yapılan değişikliklerin ve Aspose.Diagram for .NET numaralı telefona yapılan geriye dönük uyumlu olmayan değişikliklerin bir listesi bulunmaktadır. Listelenen herhangi bir değişiklikle ilgili endişeleriniz varsa lütfen the[Aspose.Diagram destek forumu](https://forum.aspose.com/c/diagram/17).
### **Diagram'de GetDefaultFontDir ekler**
Varsayılan Yazı Tipleri klasör yolunu alın

{{< highlight "java" >}}

  string str =  diagram.GetDefaultFontDir();

{{< /highlight >}}
