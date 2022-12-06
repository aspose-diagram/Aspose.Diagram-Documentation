---
title: Aspose.Diagram for .NET 20.5 Sürüm Notları
type: docs
weight: 30
url: /tr/net/aspose-diagram-for-net-20-5-release-notes/
---
{{% alert color="primary" %}} 

Bu sayfa Aspose.Diagram for .NET 20.5 için sürüm notları bilgilerini içerir.

{{% /alert %}} 
## **İyileştirmeler ve Değişiklikler**
VSD'den PDF'e dönüştürme, şekillerin doğru metin hizalaması korunmaz

|**Anahtar**|**Özet**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51088|VSD'in yanlış sayfa sayısını alır|Artırma|
|DIAGRAMNET-51731|diagram'de bir şeklin başka bir şekille kesişip kesişmediğini belirleme|Artırma|
|DIAGRAMNET-51833|Aspose.Diagram 20.4: Visio Belge sürümü desteklenmiyor|Artırma|
|DIAGRAMNET-50361|VSD'den PDF'e dönüştürme, şekillerin doğru metin hizalaması korunmaz|Böcek|
|DIAGRAMNET-50955|VSDX PNG'ye dönüştürülürken baklava şekillerinin metin öğelerinin yeri değiştiriliyor|Böcek|
|DIAGRAMNET-50990|Artı, bir VSDX'i PNG'ye dönüştürürken negatif ve dolar işaretleri düzgün şekilde hizalanmaz|Böcek|
|DIAGRAMNET-51815|Şekildeki büyük miktarda metin satırı, alt tarafta açıkça yer değiştirmeye neden olabilir|Böcek|
|DIAGRAMNET-51820|Değerlendirme filigranı bir sayfaya sığmıyor|Böcek|
|DIAGRAMNET-51821|Visio'den Html'ye - çıktıdaki görüntü ve bağlantı sorunları|Böcek|
|DIAGRAMNET-51823|Visio'i SVG'ye dönüştürürken. Bazı resimlerde sorun var Simge Eksik|Böcek|
|DIAGRAMNET-51824|Visio'i SVG'ye dönüştürürken. İçerik Hizalaması yanlış|Böcek|
|DIAGRAMNET-51826|Visio'i SVG'ye dönüştürürken. Simge Eksik|Böcek|
|DIAGRAMNET-51827|Visio'i SVG'ye dönüştürürken - QR Kodu Eksik|Böcek|
|DIAGRAMNET-51828|Visio'i SVG'ye dönüştürürken - PDF simgesi Eksik|Böcek|
|DIAGRAMNET-51829|Visio'i SVG'ye dönüştürürken - Simge kayboldu (Eksik)|Böcek|
|DIAGRAMNET-51830|Visio'i SVG'ye dönüştürürken - Görüntü kayboldu (Eksik)|Böcek|
|DIAGRAMNET-51831|Visio'den HTML'ye - çıktıdaki resim ve bağlantı sorunları|Böcek|
|DIAGRAMNET-51834|Visio HTML kaydet - yanlış bağlayıcılar|Böcek|

## **Herkese Açık API ve Geriye Dönük Uyumsuz Değişiklikler**
Aşağıda, API numaralı telefon numarasına eklenen, yeniden adlandırılan, kaldırılan veya kullanımdan kaldırılan üyeler gibi genele açık olarak yapılan tüm değişikliklerin ve Aspose.Diagram for .NET numaralı telefona yapılan geriye dönük uyumlu olmayan değişikliklerin bir listesi bulunmaktadır. Listelenen herhangi bir değişiklikle ilgili endişeleriniz varsa lütfen şu adrese bildirin: Aspose.Diagram destek forumu.
### **IsIntersect'i Şekle Ekler**
- Bu şeklin başka bir şekille kesişip kesişmediğini gösterir.

{{< highlight "java" >}}

Shape s1 = diagram.Pages[0].Shapes.GetShape(1);

Shape s2 = diagram.Pages[0].Shapes.GetShape(2);

bool isIntersect = s1.IsIntersect(s2);

{{< /highlight >}}



