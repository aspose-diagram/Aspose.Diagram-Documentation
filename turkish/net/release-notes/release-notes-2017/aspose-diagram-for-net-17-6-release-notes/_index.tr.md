---
title: Aspose.Diagram for .NET 17.6 Sürüm Notları
type: docs
weight: 70
url: /tr/net/aspose-diagram-for-net-17-6-release-notes/
---
{{% alert color="primary" %}} 

 Bu sayfa için sürüm notları içerir[Aspose.Diagram for .NET 17.6](https://www.nuget.org/packages/Aspose.Diagram/17.6.0).

{{% /alert %}} 
## **İyileştirmeler ve Değişiklikler**

|**Anahtar**|**Özet**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51264|VSDM'i SVG'ye dönüştürürken şekillerin gölgesi siyahtır|Artırma|
|DIAGRAMNET-51270|Visio Viewer'da VSDX şekli görülemiyor|Artırma|
|DIAGRAMNET-51273|Visio Viewer 2013'te şeklin yanlış görüntülenmesi|Artırma|
|DIAGRAMNET-51249|VSDM'de bağlanan kavisli hattın yanlış görünümü|Böcek|
|DIAGRAMNET-51250|VSD'i PDF'ye dönüştürürken metne ek bir sol parantez eklenir|Böcek|
|DIAGRAMNET-51251|Bir VSDM, SVG'ye dönüştürülürken simgenin boyutu düşürüldü|Böcek|
|DIAGRAMNET-51253|VSDM'i SVG'ye dönüştürürken şekillerdeki metin ve kenarlıkların yanlış rengi|Böcek|
|DIAGRAMNET-51255|VSDM, SVG'ye dönüştürülürken alttaki bir resim ezildi|Böcek|
|DIAGRAMNET-51258|VSDM rutinini açın ve kaydedin - duvarların uzunluğu değiştirilir|Böcek|
|DIAGRAMNET-51259|VSDM rutinini açın ve kaydedin - duvarların uzunluğu değiştirilir|Böcek|
|DIAGRAMNET-51260|Diagram sınıfının düzen yöntemi çağrılırken dizin çıkış aralığı hatası oluştu|Böcek|
|DIAGRAMNET-51263|VSDM'i SVG'ye dönüştürürken ek bir kırmızı renk etiketi görünür|Böcek|
|DIAGRAMNET-51265|Başlık metninin yazı tipi, bir VSDM'in SVG'ye dönüştürülmesinde değiştirilir|Böcek|
|DIAGRAMNET-51266|Arka plan görüntüsünün boyutu, VSDM'i SVG'ye dönüştürmek için azaltıldı|Böcek|
|DIAGRAMNET-51267|VSDM, SVG'ye dönüştürülürken bir simge boyutu küçültülür|Böcek|
|DIAGRAMNET-51268|VSDM çiziminden bir görüntünün yanlış saydamlık değerini alır|Böcek|
|DIAGRAMNET-51269|Sanallaştırma koruması ekleyin|Böcek|
## **Herkese Açık API ve Geriye Dönük Uyumsuz Değişiklikler**
Aşağıda, API numaralı telefon numarasına eklenen, yeniden adlandırılan, kaldırılan veya kullanımdan kaldırılan üyeler gibi genele açık olarak yapılan değişikliklerin ve Aspose.Diagram for .NET numaralı telefona yapılan geriye dönük uyumlu olmayan değişikliklerin bir listesi bulunmaktadır. Listelenen herhangi bir değişiklikle ilgili endişeleriniz varsa lütfen the[Aspose.Diagram destek forumu](https://forum.aspose.com/c/diagram/17).
### **Shape Sınıfına RefreshData Üyesi ekler**
Shape sınıfı örneğinin RefreshData yöntemi, şeklin metnini veya diğerlerini değiştirdikten sonra XForm, TextXForm, Connection ve Geom dahil olmak üzere şeklin verilerini yeniler.

{{< highlight "java" >}}

 // Load diagram

Diagram diagram = new Diagram(@"c:\temp\3DShape_Rotation.vsdx");

// get page by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// get shape by ID

Aspose.Diagram.Shape shape = page.Shapes.GetShape(1);

// set PinX and PinY values

shape.XForm.PinX.Value = 5;

shape.XForm.PinY.Value = 5;

// save diagram to VSDX format

diagram.Save(@"c:\temp\3DShape_Rotation_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
