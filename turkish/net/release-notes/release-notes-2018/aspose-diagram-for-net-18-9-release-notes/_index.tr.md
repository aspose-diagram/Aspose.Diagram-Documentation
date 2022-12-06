---
title: Aspose.Diagram for .NET 18.9 Sürüm Notları
type: docs
weight: 40
url: /tr/net/aspose-diagram-for-net-18-9-release-notes/
---
{{% alert color="primary" %}} 

 Bu sayfa için sürüm notları içerir[Aspose.Diagram for .NET 18.9](https://www.nuget.org/packages/Aspose.Diagram/18.9.0).

{{% /alert %}} 
## **İyileştirmeler ve Değişiklikler**

|**Anahtar**|**Özet**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51509|VSDX'den PNG'ye - Çıktı görüntüsünde satır opaklığı kayboldu|Artırma|
|DIAGRAMNET-51510|VSDX - SVG - Çıktı görüntüsünde çizgi opaklığı kayboldu|Artırma|
|DIAGRAMNET-51516|Birden Çok VISIO dosyasını tek bir çıktıda birleştirin|Artırma|
|DIAGRAMNET-50272|VSD - SVG dönüşümü - Bazı bağlantı noktalarının konumu ve boyutu yanlış|Böcek|
|DIAGRAMNET-50273|VSD'den SVG'ye - Şekil metni öğelerinin hizalaması yanlış|Böcek|
|DIAGRAMNET-50487|VSD'den HTML'ye - Değer arasındaki eğik çizgi karakteri yanlış yerleştirilmiş|Böcek|
|DIAGRAMNET-50975|VSDX'den PDF'ye - Şeklin arka plan rengi siyah|Böcek|
|DIAGRAMNET-50976|VSDX'den HTML'ye - Şeklin arka plan rengi siyah|Böcek|
|DIAGRAMNET-50980|VSDX'den PNG'ye - Baklava şekillerinin içindeki sayılar yanlış yerleştirilmiş|Böcek|
|DIAGRAMNET-51129|Bir VSD'i PDF'ye dönüştürürken metin öğeleri düzgün şekilde hizalanmıyor|Böcek|
|DIAGRAMNET-51511|PNG dönüştürmede ek ok uçları|Böcek|
|DIAGRAMNET-51512|SVG dönüşümünde gösterilen ek ok uçları|Böcek|
## **Herkese Açık API ve Geriye Dönük Uyumsuz Değişiklikler**
Aşağıda, API numaralı telefon numarasına eklenen, yeniden adlandırılan, kaldırılan veya kullanımdan kaldırılan üyeler gibi genele açık olarak yapılan değişikliklerin ve Aspose.Diagram for .NET numaralı telefona yapılan geriye dönük uyumlu olmayan değişikliklerin bir listesi bulunmaktadır. Listelenen herhangi bir değişiklikle ilgili endişeleriniz varsa lütfen the[Aspose.Diagram destek forumu](https://forum.aspose.com/c/diagram/17).
#### **Diagram Sınıfında Combine yöntemi eklendi**
Bir Diagram nesnesini başka bir Diagram nesnesiyle birleştirir.

{{< highlight "java" >}}

             Diagram diagramF = new Diagram( "f.vsdx");

            Diagram diagramS = new Diagram( "s.vsdx");

            diagramF.Combine(diagramS);

{{< /highlight >}}
