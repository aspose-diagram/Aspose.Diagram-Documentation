---
title: Aspose.Diagram for .NET 17.8 Sürüm Notları
type: docs
weight: 50
url: /tr/net/aspose-diagram-for-net-17-8-release-notes/
---
{{% alert color="primary" %}} 

 Bu sayfa için sürüm notları içerir[Aspose.Diagram for .NET 17.8](https://www.nuget.org/packages/Aspose.Diagram/17.8.0).

{{% /alert %}} 
## **İyileştirmeler ve Değişiklikler**

|**Anahtar**|**Özet**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51295|VSDX'den SVG'ye - SVG çıktısının düşük kalitesi.|Artırma|
|DIAGRAMNET-51298|SVGSaveOptions - bitmap sıkıştırma düzeyini kontrol etmek için destek ekleyin.|Artırma|
|DIAGRAMNET-51300|Bağlantı dizini ile şekilleri bağlama desteği ekleyin.|Artırma|
|DIAGRAMNET-50577|VSDX'den PDF'e dönüştürme, dairesel şeklin metni yanlış yerleştirilmiş - I.|Böcek|
|DIAGRAMNET-50582|VSDX'den HTML'ye dönüştürme, dairesel şeklin metni yanlış yerleştirilmiş - I.|Böcek|
|DIAGRAMNET-50601|VSDX'den PDF'e dönüştürme, dairesel şeklin metni yanlış yerleştirilmiş - II.|Böcek|
|DIAGRAMNET-50606|VSDX'den HTML'ye dönüştürme, dairesel şeklin metni yanlış yerleştirilmiş - II.|Böcek|
|DIAGRAMNET-51197|VSDM'in SVG'ye kaydedilmesinde uyarı üçgeni şekilleri doğru şekilde oluşturulmuyor.|Böcek|
|DIAGRAMNET-51245|VSD'i PDF'ye dönüştürürken yer değiştiren metin öğeleri.|Böcek|
|DIAGRAMNET-51246|VSD'i PDF'ye dönüştürürken metne yanlış yazı tipleri uygulandı.|Böcek|
|DIAGRAMNET-51296|VSDM'den SVG'ye - görüntü kesilir.|Böcek|
|DIAGRAMNET-51301|VSDX'den PDF'e - bağlantı çizgilerindeki metnin rengi değiştirildi.|Böcek|
|DIAGRAMNET-51302|VSDX'den PDF'ye - eksik grafik öğeleri.|Böcek|
|DIAGRAMNET-51304|VSDX'den PDF'ye - akış şemasının eksik oluşturulması.|Böcek|
|DIAGRAMNET-51305|VSDX'den PDF'ye - eksik grafik öğeleri.|Böcek|
|DIAGRAMNET-51306|VSDX'den PDF'e - bağlantı çizgilerindeki metnin rengi değiştirildi.|Böcek|
|DIAGRAMNET-51307|VSDX'den PDF'ye - eksik grafik öğeleri.|Böcek|
|DIAGRAMNET-51313|VSDX çiziminin açma ve kaydetme rutini bozuk bir çıktı dosyası oluşturuyor.|Böcek|
|DIAGRAMNET-51314|VSDX'den SVG'ye - metnin yanlış konumlandırılması.|Böcek|
|DIAGRAMNET-51317|VSDX'den PDF'e - bağlantı satırlarının metni eksik.|Böcek|
|DIAGRAMNET-51318|VSDX'den PDF'ye - dikdörtgen şekillerin kalın biçimlendirilmiş metni eksik.|Böcek|
|DIAGRAMNET-51319|VSDM'den SVG'ye - aritmetik işlem taşma hatasıyla sonuçlandı.|Böcek|
|DIAGRAMNET-51320|VSDM yüklenirken şekil öğesinde hata oluştu.|Böcek|
|DIAGRAMNET-51323|VSDM - SVG - tüm bağlantı hatları eksik.|Böcek|
|DIAGRAMNET-51324|VSDM'den SVG'ye - çeşitli şekillerde yanlış kenarlık stili ve kenarlık rengi.|Böcek|
|DIAGRAMNET-51326|Şekle iki yorum ekledikten sonra sorun.|Böcek|
|DIAGRAMNET-51327|Çeşitli şekillere yorum eklerken "AddComment" yöntemini kullandıktan sonra sorun.|Böcek|
|DIAGRAMNET-51328|Aspose Diagram, şekli belgeye hatalı bir şekilde aktarıyor.|Böcek|
|DIAGRAMNET-51330|VSDM'den SVG'ye - ek bir filigran metni eklenir.|Böcek|
|DIAGRAMNET-51332|VSDM'den SVG'ye - bir simgenin yanlış oluşturulması.|Böcek|
|DIAGRAMNET-51334|VSDM'den SVG'ye - sağ üst köşedeki kaydırılmış metin.|Böcek|
|DIAGRAMNET-51335|VSDM'den SVG'ye - arka plan görüntüsünün hatalı oluşturulması.|Böcek|
|DIAGRAMNET-51337|VSD'den HTML'ye - giriş dizisi hatasının geçersiz biçimi.|Böcek|
## **Herkese Açık API ve Geriye Dönük Uyumsuz Değişiklikler**
Aşağıda, API numaralı telefon numarasına eklenen, yeniden adlandırılan, kaldırılan veya kullanımdan kaldırılan üyeler gibi genele açık olarak yapılan değişikliklerin ve Aspose.Diagram for .NET numaralı telefona yapılan geriye dönük uyumlu olmayan değişikliklerin bir listesi bulunmaktadır. Listelenen herhangi bir değişiklikle ilgili endişeleriniz varsa lütfen the[Aspose.Diagram destek forumu](https://forum.aspose.com/c/diagram/17).
### **SVGSaveOptions sınıfına Quality üyesi ekler**
Oluşturulan görüntülerin kalitesini belirleyen bir değer alır veya ayarlar.

{{< highlight "java" >}}

 string dataDir = @"c:\temp\";

// Load an existing drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify SVG export settings

SVGSaveOptions options = new SVGSaveOptions();

// set image quality

options.Quality = 100;

// save drawing in the SVG format

diagram.Save(dataDir + "UseSVGSaveOptions_out.svg", options);

{{< /highlight >}}
### **Page sınıfına ConnectShapesViaConnectorIndex yöntemini ekler**
Bağlantı dizinlerini kullanarak şekillerin bağlanmasına izin verir.

{{< highlight "java" >}}

 string dataDir = @"c:\temp\";

// Load an existing drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get shapes by ID

Aspose.Diagram.Shape shape1 = diagram.Pages[0].Shapes.GetShape(1);

Aspose.Diagram.Shape shape2 = diagram.Pages[0].Shapes.GetShape(2);

// add connector shapes

Aspose.Diagram.Shape connector1 = new Aspose.Diagram.Shape();

long connecter1Id = diagram.AddShape(connector1, "Dynamic connector", 0);

// connect shapes by index of conneecting points

diagram.Pages[0].ConnectShapesViaConnectorIndex(shape1.ID, 6, shape2.ID, 3, connecter1Id);

// save drawing

diagram.Save(dataDir + "UseSVGSaveOptions_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Kullanım Örnekleri**
Lütfen Aspose.Diagram Wiki belgelerine eklenen yardım konularının listesini kontrol edin:

1. [Şekilleri bağlamak için Bağlantı dizinlerini kullanın](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/#use-connection-indexes-to-connect-shapes)
1. [SVG Kaydetme Seçeneklerinin Kullanımı](https://docs.aspose.com/diagram/net/save-visio-document/)
