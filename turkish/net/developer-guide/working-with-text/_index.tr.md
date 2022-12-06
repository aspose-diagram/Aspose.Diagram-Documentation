---
title: Metinle Çalışmak
type: docs
weight: 90
url: /tr/net/working-with-text/
description: Bu bölüm, Aspose.Diagram ile bir metin şeklinin nasıl ekleneceğini veya şeklin metninin nasıl güncelleneceğini açıklar.
---
## **Visio Sayfasına Metin Şekli Ekleme**
 Aspose.Diagram API, geliştiricilerin Visio sayfasında herhangi bir yere bir metin şekli eklemesine olanak tanır. Bunu başarmak için, AddText yöntemi[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page) sınıf, PinX, PinY, genişlik, yükseklik ve metin parametrelerini alır.
### **Bir Metin Şekli Programlama Örneği Ekleme**
Aşağıdaki kod parçası, Visio diagram'de bir metin şekli ekler.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-InsertTextShape-InsertTextShape.cs" >}}
## **Güncelleme Visio Şekil Metni**
 Birlikte[diyagramlar oluşturma](/diagram/tr/net/load-or-create-a-visio-drawing/) , Aspose.Diagram for .NET, şekillerle farklı şekillerde çalışmanızı sağlar. Bu makalede, şekillerdeki metne nasıl erişileceği ve bu metnin nasıl güncelleneceği ele alınmaktadır. Tarafından sunulan Text özelliği[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) sınıfı, Aspose.Diagram.Text nesnesini destekler. Özellik, bir şeklin metnini almak veya güncellemek için kullanılabilir. Bir şeklin metnini güncelleme işlemi basittir:

1. diagram yükleyin.
1. Belirli bir şekil bulun.
1. Yeni metni ayarlayın.
1. diagram'i kaydedin.
### **Shape Text Programlama Örneği Güncelleme**
Aşağıdaki kod parçası bir şeklin metnini günceller. Şekiller kimlikleri ile tanımlanır. Aşağıdaki kod parçaları, işlem adı verilen ve kimliği 1 olan bir şekli arar ve metnini değiştirir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-UpdateShapeText-UpdateShapeText.cs" >}}
## **Visio Şekline Yerleşik veya Özel Stil Sayfası Uygulayın**
Microsoft Visio stil sayfaları, tutarlı bir görünüm ve his için şekillere uygulanabilen biçimlendirme bilgilerini saklar. Aspose.Diagram for .NET, bir uygulamanın içinden stil sayfaları uygulamanıza olanak tanır.

 tarafından sunulan TextStyle, FillStyle ve LineStyle özellikleri[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) sınıf desteği[Aspose.Diagram.StyleSheet](http://www.aspose.com/api/net/diagram/aspose.diagram/stylesheet) nesne. Özellik, stil bilgilerini almak ve bir diagram'e özel metin, çizgi ve dolgu stilleri uygulamak için kullanılabilir.
### **Microsoft Visio'deki Özel Stiller**
Microsoft Visio'deki şekillere özel stiller uygulamak için:

1. Microsoft Visio'de bir diagram açın.
1.  Seçme**Stilleri Tanımla** dan**Biçim** menüsü (Visio 2007) veya sağ tıklayın**stiller** içinde**Çizim Gezgini** penceresini açın ve seçin**Stilleri Tanımla** (Visio 2010).
1.  İçinde**Stilleri Tanımla** iletişim kutusunda, özel stil sayfanız için yeni bir ad yazın. Örneğin, CustomStyle1.
1.  Tıkla**Metin**, **Astar** ve**Doldurmak** Sırasıyla metin, çizgi ve dolgu stillerini ayarlamak için düğmeler.
1.  Tıklamak**TAMAM**.

Microsoft Visio'de özel stil sayfaları tanımladıktan sonra, şekillerinize özel stiller uygulamak için bir .NET uygulamasında aşağıdaki kodu kullanın. Aşağıdaki kod örneklerinin yukarıda tanımlanan özel stil sayfasını çağırdığını unutmayın: uyguladığınız sayfanın adını ve konumunu bilmeniz gerekir. Özel stilleri programlı olarak uygulamak için:

1. diagram yükleyin.
1. Stil uygulamak istediğiniz şekli bulun.
1. Stil sayfasını yükleyin.
1. Stilleri uygulayın.
1. diagram'i kaydedin.
#### **Özel Stiller Programlama Örneği Uygula**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-ApplyCustomStyleSheets-ApplyCustomStyleSheets.cs" >}}
## **Bir Şeklin Her Metin Değerine Farklı Stil Uygulayın**
 Birlikte[diyagramlar oluşturma](/diagram/tr/net/load-or-create-a-visio-drawing/), Aspose.Diagram for .NET, şekillerle farklı şekillerde çalışmanızı sağlar. Bu makale, bir şekle birden çok metin değeri eklemeye ve her metin değerine farklı stil uygulamaya yardımcı olur.

{{% alert color="primary" %}} 

Shape öğesi, metnin karakterlerini ve bir çalıştırmanın sonunu ve sonrakinin başlangıcını işaretleyen özel öğeleri (cp, pp, tp ve fld) içeren Metin adlı bir öğe içerir. Karakter Öğesi, şeklin metni için yazı tipi, renk, metin stili, büyük/küçük harf, taban çizgisine göre konum ve punto boyutu gibi biçimlendirme niteliklerini içerir.

{{% /alert %}} 
### **Şekil Metni ve Stilleri Ekleme**

|**Giriş diagram**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](working-with-text_1.png)|


|**Diagram her metin değerinde farklı stile sahip bir şekle çeşitli metin değerleri ekledikten sonra**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](working-with-text_2.png)|
#### **Metin ve Stiller Programlama Örneği Ekleme**
Aşağıdaki kod parçası, bir şeklin metnini ve farklı stilleri ekler.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-ApplyFontOnText-ApplyFontOnText.cs" >}}
## **Bir Şeklin Metnini Bul ve Değiştir**
 bu[Txt](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) Class, şeklin metnini düzenlemenizi sağlar. Tarafından sunulan replace yöntemi[Txt](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) sınıf, bir şeklin metnini değiştirmeyi destekler.
Bu makaledeki kod örnekleri, sayfadaki şeklin metnini bulur ve değiştirir.

|**Giriş diagram**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](working-with-text_3.png)|


|**Şekil düzenlendikten sonra diagram**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](working-with-text_4.png)|
Şeklin metnini değiştirme süreci:

1. diagram yükleyin.
1. Bir şeklin belirli bir metnini bulun.
1. Bu şeklin metnini değiştir
1. diagram'i kaydedin.
### **Metin Programlama Örneği Bul ve Değiştir**
Aşağıdaki kod parçacıkları, şeklin metninin nasıl değiştirileceğini gösterir. Kod, bir sayfanın şekillerini yineler.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-FindAndReplaceShapeText-FindAndReplaceShapeText.cs" >}}
## **Visio Diagram Sayfasından Düz Metni Çıkarın**
Aspose.Diagram API, geliştiricilerin Visio diagram sayfasından düz metin çıkarmasına olanak tanır. Ayrıca Visio diagram metninin tamamını kapsayacak şekilde Visio diagram sayfalarını yineleyebilirler.

 Microsoft Office Visio yazıları şekillere ekliyor. bu[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, metnin karakterlerini ve bir çalıştırmanın sonunu ve sonrakinin başlangıcını işaretleyen özel öğeleri (cp, pp, tp ve fld) içeren Metin adlı bir öğe içerir.
### **Düz Metin Programlama Örneği Çıkarın**
Aşağıdaki kod parçası, Visio Sayfasının şekillerini yineler ve biçimlendirme bilgisi olmadan düz metni filtreler.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-GetPlainTextOfVisio-GetPlainTextOfVisio.cs" >}}
