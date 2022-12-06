---
title: Aspose.Diagram for .NET 20.8 Sürüm Notları
type: docs
weight: 14
url: /tr/net/aspose-diagram-for-net-20-8-release-notes/
---
{{% alert color="primary" %}}

Bu sayfa Aspose.Diagram for .NET 20.8 için sürüm notları bilgilerini içerir.

{{% /alert %}}
## **İyileştirmeler ve Değişiklikler**  ##

|**Anahtar**|**Özet**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51886|Sözcükler, Hücreler, Slaytlar vb. Ole nesnesini Diagram'e hem nesne verileri hem de içindeki önizleme görüntüsü ile tek bir şekle ekleme yeteneği oluşturun.|Artırma|
|DIAGRAMNET-51888|Visio'den PDF'e - API'in dönüştürülmesi uzun zaman alıyor|Artırma|
|DIAGRAMNET-51889|20 dakikadan fazla pdf döngüsüne kaydetme|Artırma|
|DIAGRAMNET-51893|VSDX'den SVG'ye dönüştürmeden sonra viewBox özelliği eksik|Artırma|
|DIAGRAMNET-51851|VSDX'den PDF'e - bazı simgeler eksik ve bazıları doğru şekilde oluşturulmamış|Böcek|
|DIAGRAMNET-51873|VSDX'den PDF'e - Çıktı PDF'sinde içerik solda görünüyor|Böcek|
|DIAGRAMNET-51874|VSDX'den PDF'ye - çıktıda içerik ve satırlar eksik|Böcek|
|DIAGRAMNET-51876|VSDX'den PNG'ye - çıktıda bazı şekiller yanlış|Böcek|
|DIAGRAMNET-51879|Visio'den PDF'e - çıktı doğru değil|Böcek|
|DIAGRAMNET-51894|diagram yüklenirken System.NullReferenceException|Böcek|
|DIAGRAMNET-51895|SelectionModel, DisplayMode gibi Grup Özelliği verileri alınamıyor|Böcek|

## **Genel API ve Geriye Dönük Uyumsuz Değişiklikler**  ##
Aşağıda, API numaralı telefon numarasına eklenen, yeniden adlandırılan, kaldırılan veya kullanımdan kaldırılan üyeler gibi genele açık olarak yapılan tüm değişikliklerin ve Aspose.Diagram for .NET numaralı telefona yapılan geriye dönük uyumlu olmayan değişikliklerin bir listesi bulunmaktadır. Listelenen herhangi bir değişiklikle ilgili endişeleriniz varsa lütfen şu adrese bildirin: Aspose.Diagram destek forumu.

####  Sayfaya Yöntem AddShape Eklendi ####
```
Diagram diagram = new Diagram();

// Get page object by index
Aspose.Diagram.Page page0 = diagram.Pages[0];
// set pinX, pinY, width and height
double pinX = 2, pinY = 2, width = 4, hieght = 3;

// Import ole as Visio shape word
page0.AddShape(pinX, pinY, width, hieght, new FileStream( "imageword.emf", FileMode.OpenOrCreate), new FileStream( "wordsource.doc", FileMode.OpenOrCreate));
```
