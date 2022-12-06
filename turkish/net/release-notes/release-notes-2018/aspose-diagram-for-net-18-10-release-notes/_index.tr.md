---
title: Aspose.Diagram for .NET 18.10 Sürüm Notları
type: docs
weight: 30
url: /tr/net/aspose-diagram-for-net-18-10-release-notes/
---
{{% alert color="primary" %}} 

 Bu sayfa için sürüm notları içerir[Aspose.Diagram for .NET 18.10](https://www.nuget.org/packages/Aspose.Diagram/18.10.0).

{{% /alert %}} 
## **İyileştirmeler ve Değişiklikler**

|**Anahtar**|**Özet**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51527|VSDM'i SVG'ye dönüştürdükten sonra görüntüler kayboluyor|Artırma|
|DIAGRAMNET-51532|VSD'den PDF'ye - Görüntünün gölgesi doğru değil|Artırma|
|DIAGRAMNET-51536|Şeklin gölgesi, VSDX'den sonra SVG Dönüşümüne kaldırıldı|Artırma|
|DIAGRAMNET-51544|Alt çizgi, VSDM'i SVG'ye dönüştürdükten sonra metinden kaldırılıyor|Artırma|
|DIAGRAMNET-51558|Shape.ConnectorsType için Getter'ı uygulayın|Artırma|
|DIAGRAMNET-51520|VDX'den HTML'ye - Çıktıda fazladan satırlar görünüyor|Böcek|
|DIAGRAMNET-51521|diagram'deki yazı tipi, VSD'i VSDX olarak kaydettikten sonra değişiklikleri alır|Böcek|
|DIAGRAMNET-51523|VSDX - SVG - Ok başları eksik|Böcek|
|DIAGRAMNET-51524|VSDM - SVG - Çıktı dosyasında Mavi Haçlar belirdi|Böcek|
|DIAGRAMNET-51525|Karar şekli elmastan kareye, VSDM'den SVG'ye dönüştürülürken değişir|Böcek|
|DIAGRAMNET-51528|Karar şekli elmastan kareye, VSDM'den SVG'ye dönüştürülürken değişir|Böcek|
|DIAGRAMNET-51529|VSDM'den SVG'ye - Noktalı çizgiler dolu çizgilere dönüştürülür|Böcek|
|DIAGRAMNET-51531|VSDX'i SVG'ye dönüştürdükten sonra şekiller sağ tarafa kaydırılıyor|Böcek|
|DIAGRAMNET-51533|Kızıl Haçlar, VISIO'dan SVG'ye Dönüştürmeden sonra ortaya çıktı|Böcek|
|DIAGRAMNET-51534|Şeklin sol alt köşesinde kırmızı nokta belirdi|Böcek|
|DIAGRAMNET-51538|VSDX'i PDF'ye dönüştürdükten sonra resimler kayboluyor|Böcek|
|DIAGRAMNET-51541|VSDX'i SVG'ye dönüştürdükten sonra metin görünmez oluyor|Böcek|
|DIAGRAMNET-51542|Metin, VSDX'den SVG'ye Dönüştürmeden sonra silindi|Böcek|
|DIAGRAMNET-51543|VSDM TO SVG'den sonra saat ve tarih biçimi değiştirilir|Böcek|
|DIAGRAMNET-51545|VSDX'den SVG'ye - Metin çıktıya kaydırılır|Böcek|
|DIAGRAMNET-51546|VSDX'den SVG'ye - Metin çıktıya kaydırılır|Böcek|
|DIAGRAMNET-51547|VSDX'den SVG'ye - Metin çıktıya kaydırılır|Böcek|
|DIAGRAMNET-51548|VSDX'den SVG'ye - Metin çıktıya kaydırılır|Böcek|
|DIAGRAMNET-51551|Şekillerin doğru tema rengi alınamıyor|Böcek|
|DIAGRAMNET-51552|SVG dönüşümünde gösterilen ters ok uçları|Böcek|
|DIAGRAMNET-51559|VSDM'i SVG'ye dönüştürürken Metin Yeniden Boyutlandırma sorunu|Böcek|
|DIAGRAMNET-51560|Bağlayıcı Çizgiler, SVG'ye dönüştürüldükten sonra inceliyor|Böcek|
## **Herkese Açık API ve Geriye Dönük Uyumsuz Değişiklikler**
Aşağıda, API numaralı telefon numarasına eklenen, yeniden adlandırılan, kaldırılan veya kullanımdan kaldırılan üyeler gibi genele açık olarak yapılan değişikliklerin ve Aspose.Diagram for .NET numaralı telefona yapılan geriye dönük uyumlu olmayan değişikliklerin bir listesi bulunmaktadır. Listelenen herhangi bir değişiklikle ilgili endişeleriniz varsa lütfen the[Aspose.Diagram destek forumu](https://forum.aspose.com/c/diagram/17).
#### **Şekilde InheritLine eklendi**
Üst stil ve ana şekil tarafından devralınan şeklin çizgi biçimlendirme değerlerini içerir.

{{< highlight "java" >}}

 		Line line = shape.InheritLine;

{{< /highlight >}}


#### **Şekilde GetConnectorsType eklendi**
Bağlayıcı türünü al

{{< highlight "java" >}}

 Shapes.GetShape(1).GetConnectorsType()

{{< /highlight >}}

