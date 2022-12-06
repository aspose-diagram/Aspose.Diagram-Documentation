---
title: Aspose.Diagram for .NET 18.1 Sürüm Notları
type: docs
weight: 120
url: /tr/net/aspose-diagram-for-net-18-1-release-notes/
---
{{% alert color="primary" %}} 

 Bu sayfa için sürüm notları içerir[Aspose.Diagram for .NET 18.1](https://www.nuget.org/packages/Aspose.Diagram/18.1.0).

{{% /alert %}} 
## **İyileştirmeler ve Değişiklikler**

|**Anahtar**|**Özet**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-50494|diagram sayfasını çoğaltmak / klonlamak için destek ekleyin|Artırma|
|DIAGRAMNET-51057|VSDM'den bir sayfa kaldırıldıktan sonra komut düğmesi kayboluyor|Artırma|
|DIAGRAMNET-51422|VSDX'den PDF'ye - proses şekillerinde gölgeler göz ardı ediliyor|Artırma|
|DIAGRAMNET-50467|VSD'den PDF'e dönüştürme, şirket kurumsal logosu yanlış yerleştirilmiş|Böcek|
|DIAGRAMNET-50469|VSD'den PDF'e dönüştürme, radyo şekli metni normalden biraz daha yüksek|Böcek|
|DIAGRAMNET-51199|VSDM'i SVG'ye kaydederken başlık metni hizalı değil|Böcek|
|DIAGRAMNET-51388|vsdx dosyalarının yüklenmesi ve kaydedilmesiyle ilgili sorunlar|Böcek|
|DIAGRAMNET-51398|VSD'den PNG'ye - metin konumu yanlış|Böcek|
|DIAGRAMNET-51407|VSD'den JPEG'e - metin öğeleri yanlış yerleştirilmiş|Böcek|
|DIAGRAMNET-51419|vsdx dosyasında şekiller düzgün bir şekilde yeniden boyutlandırılmıyor|Böcek|
|DIAGRAMNET-51420|VSDX dosyası yüklenip kaydedildikten sonra bozuluyor|Böcek|
|DIAGRAMNET-51421|VSDX'den PDF'ye - metnin yazı tipi rengi yanlış|Böcek|
## **Herkese Açık API ve Geriye Dönük Uyumsuz Değişiklikler**
Aşağıda, API numaralı telefon numarasına eklenen, yeniden adlandırılan, kaldırılan veya kullanımdan kaldırılan üyeler gibi genele açık olarak yapılan değişikliklerin ve Aspose.Diagram for .NET numaralı telefona yapılan geriye dönük uyumlu olmayan değişikliklerin bir listesi bulunmaktadır. Listelenen herhangi bir değişiklikle ilgili endişeleriniz varsa lütfen the[Aspose.Diagram destek forumu](https://forum.aspose.com/c/diagram/17).
### **Page sınıfına Copy üyesi ekler**
Copy üyesi, bu sayfayı klonlamak için bir parametre olarak bir hedef sayfa örneği alır.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// copy diagram

newPage.Copy(diagram.Pages[0]);

{{< /highlight >}}
### **Kullanım Örnekleri**
Lütfen Aspose.Diagram Wiki belgelerine eklenen yardım konularının listesini kontrol edin:

1. [Visio Sayfasını başka bir Sayfa örneğine kopyalayın](https://docs.aspose.com/diagram/net/retrieve-get-copy-and-insert-a-page/#copy-visio-page-to-another-page-instance)
