---
title: Visio Şekil Verilerini Ekleme, Alma, Kopyalama ve Okuma
type: docs
weight: 10
url: /tr/java/add-retrieve-copy-and-read-visio-shape-data/
description: Bu bölüm, Aspose.Diagram ile bir şeklin nasıl ekleneceğini, şeklin özelliğinin nasıl ayarlanacağını veya bir şeklin nasıl kopyalanacağını açıklar.
---
## **Visio'de Yeni Şekil Ekleme**
Aspose.Diagram for Java, Microsoft Visio diyagramlarını farklı şekillerde işlemenizi sağlar. Yapabileceğiniz şeylerden biri, diyagramlara yeni şekiller eklemektir. Aspose.Diagram for Java, diagram'e yeni bir şekil eklemenizi sağlar. Eklenen şekil, Aspose.Diagram for Java kullanılarak da özelleştirilebilir.

Bu konu, diagram'e yeni bir dikdörtgen şeklinin nasıl ekleneceğini açıklar.

Yeni şekiller oluşturmak için Aspose.Diagram for Java API'i kullanın ve ardından bu şekilleri diagram'in şekil koleksiyonuna ekleyin.

Yeni bir şekil eklemek için:

1. **sayfayı bul** - Her Visio diagram, bir sayfa koleksiyonu içerir. Geliştiriciler, sayfayı sayfa kimliği veya Adına göre alabilir ve gerekli sayfayı[Sayfa](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)sınıf nesnesi.
1. **Gerekli Master of a Shape'i ekleyin** - Her Visio diagram, bir usta koleksiyonu içerir. Geliştiriciler, mevcut şablon dosyasından (doğrudan yol veya dosya akışı yoluyla) bir Master (Kimlik veya Ada göre) ekleyebilir.
1. **Visio diagram'de şekil ekleyin** - Geliştiriciler, sayfa dizini (0'dan başlayarak), ana ad, PinX, PinY, yükseklik (isteğe bağlı) ve genişliğe (isteğe bağlı) göre Visio diagram'e yeni bir şekil yerleştirebilir.
1. **Şekil özelliklerini ayarla** - Diagram sınıfının AddShape yöntemi, şekil kimliğini döndürür. Geliştiriciler, bu kimliği kullanarak bir Visio diagram'den şekil alabilir ve ardından renk, konum, hizalama ve metin gibi özelliklerini ayarlayabilir.

|<p>**diagram girişi** </p><p>![yapılacaklar:resim_alternatif_Metin](add-retrieve-copy-and-read-visio-shape-data_1.png)</p>|<p>**Şekil eklenmiş diagram** </p><p>![yapılacaklar:resim_alternatif_Metin](add-retrieve-copy-and-read-visio-shape-data_2.png)</p>|
|:- |:- |
### **Programlama Örneği Ekle**
Aşağıdaki kod parçacığı, her bir adımın nasıl yapılacağını gösterir.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-AddingNewShape-AddingNewShape.java" >}}

{{% alert color="primary" %}}

 Soru ve önerilerinizi şu adrese bekliyoruz:[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Derhal cevap vereceğiz.

{{% /alert %}}
## **Şekil Bilgilerini Alma**
[Diyagramlarla Çalışmak](/diagram/tr/java/working-with-diagrams/)diyagramların nasıl oluşturulacağını, şekiller ve bağlayıcıların nasıl ekleneceğini ve ardından diagram gibi diagram öğeleri hakkında bilgilerin nasıl alınacağını açıklar.[sayfalar](/diagram/tr/java/retrieve-get-copy-and-insert-a-page/), [ustalar](https://docs.aspose.com/diagram/java/working-with-masters/), [konektörler](https://reference.aspose.com/diagram/java/com.aspose.diagram/ConnectCollection) ve[yazı tipleri](https://reference.aspose.com/diagram/java/com.aspose.diagram/FontCollection). Bu makale, bir diagram'deki şekillerle ilgili bilgilerin nasıl alınacağını ele almaktadır.

diagram'deki her şeklin bir kimliği ve adı vardır. Kimlik, Visio ile programlama yaparken önemlidir: bir şekle erişmenin ana yöntemidir. Her şekil ayrıca hangi kalıptan (şablondan) yapıldığına dair bilgileri de tutar.

 A[Şekil](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) Visio çizimindeki bir nesnedir. Page sınıfı tarafından sunulan Shapes özelliği, Aspose.Diagram.Shape nesne koleksiyonunu destekler. Shapes özelliği, bir şekil hakkında bilgi almak için kullanılabilir.

Örneğin aşağıdaki konsol penceresinde, dört şekil içeren bir diagram için bilgi çıktısını görebilirsiniz: iki sonlandırıcı, bir işlem ve bir dinamik bağlayıcı. Her birinin benzersiz bir kimliği ve ana (kalıp) şeklinin adı vardır.

|**Şekil bilgilerini gösteren bir konsol penceresi**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](add-retrieve-copy-and-read-visio-shape-data_3.png)|
Visio sayfa bilgisini almak için:

1. Bir diagram yükler.
1. diagram'deki tüm şekillerde döngü yapmak için bir foreach döngüsü kurar.
1. Şekil bilgilerini görüntüler.
### **Programlama Örneği Al**
Aşağıdaki kod parçası, şekil bilgisini bir Visio diagram'den alır.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RetrieveShapeInfo-RetrieveShapeInfo.java" >}}

## **Mevcut Bir Visio'den Şekilleri Kopyala**
Aspose.Diagram for Java API, geliştiricilerin Visio kaynak sayfasındaki şekilleri yeni Visio diagram sayfasına kopyalamasına olanak tanır. Grup şekillerinin kopyalanmasını da destekler. Bu makalede, kaynak diagram sayfasındaki tüm şekillerin nasıl kopyalanacağı açıklanmaktadır.

Şekilleri kopyalamak için geliştiriciler, şekil doldurma stilini ve diğer biçimlendirme özelliklerini korumak için PageSheet ve kaynak Visio temalarını da kopyalamalıdır.

Bu örnek şu şekilde çalışır:

1. Bir kaynak yükleyin Visio.
1. Yeni bir Visio başlat
1. Visio kaynağından ustalar ve temalar ekleyin.
1. Sayfayı Visio kaynağından alın.
1. PageSheet'ini yeni Visio Sayfasına kopyalayın.
1. Kaynak Visio sayfasının şekillerini yineleyin.
1. Yeni kimliğini ayarlayın ve yeni Visio sayfasına ekleyin.
1. Yeni Visio'i yerel depolamaya kaydedin.
### **Programlama Örneği Kopyala**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-CopyShape-CopyShape.java" >}}


{{% alert color="primary" %}}

 Soru ve önerilerinizi şu adrese bekliyoruz:[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Derhal cevap vereceğiz.

{{% /alert %}}
## **Visio Shape'i başka bir Shape örneğine kopyalama**
Shape sınıfının Copy yöntemi, klonlamak için bir şekil örneği alır.

## **Visio Şekil Verilerini Okuma**
 tarafından sergilenen Props koleksiyonu[Şekil](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) sınıfı destekler[Aspose.Diagram.Prop](http://www.aspose.com/api/java/diagram/com.aspose.diagram/prop) nesne. Özellik, bir şeklin verilerini (özel özellikler) okumak için kullanılabilir.
### **Tüm Şekil Özelliklerini Oku**
Microsoft Visio'de özel özellikleri tanımlamak için:

1. diagram'de bir şekle sağ tıklayın.
1.  Seçme**Veri** , sonra**Şekil Verisi** menüden.
 Varolan tüm özellikler iletişim kutusunda listelenir.

|**Microsoft Visio'de görüldüğü gibi bir şeklin verileri.**|** |
|:- |:- |
|![yapılacaklar:resim_alternatif_Metin](add-retrieve-copy-and-read-visio-shape-data_4.png)||


|**Şekil verisi çıktısını gösteren bir konsol penceresi.**|** |
|:- |:- |
|![yapılacaklar:resim_alternatif_Metin](add-retrieve-copy-and-read-visio-shape-data_5.png)||
#### **Programlama Örneği Oku**
Aşağıdaki kod parçacıkları, şekil verilerini (özel özellikler) okur.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ReadAllShapeProps-ReadAllShapeProps.java" >}}

### **Bir Şekil Özelliğini Ada Göre Okuma**
Aşağıdaki kod parçacığı, bir şekil özelliğini ada göre okur (özel özellik).
#### **Ada Göre Okuma Programlama Örneği**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ReadShapePropByName-ReadShapePropByName.java" >}}

## **Şekilleri bağlamak için Bağlantı dizinlerini kullanın**
Aspose.Diagram for Java API zaten geliştiricilerin şekle yeni bağlantı noktaları eklemesine izin veriyor ve geliştiriciler artık bağlantı dizinlerini kullanarak şekilleri birbirine bağlayabiliyor.
### **Şekilleri bağlamak için Bağlantı dizinlerini kullanın**
Tarafından sunulan ConnectShapesViaConnectorIndex üyesi[Sayfa](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)class, bağlantı dizinlerini kullanarak şekilleri bağlamak için kullanılabilir.

1. Yeni bir çizim başlatın.
1. Dört dikdörtgen şekli yerleştirin
1. Alt sınır çizgisinde üç bağlantı noktası olacak şekilde iki ek bağlantı noktası ekleyin
1. Her bir alt bağlantıdaki ilk şekli, dinamik bağlayıcılarla Üstteki diğer üç dikdörtgen şekle bağlayın
1. Çizimi kaydet
#### **Şekilleri bağlamak için bağlantı dizinlerini kullanın Programlama Örneği**
Aspose.Diagram for Java API ile bağlantı dizinlerini kullanarak şekilleri bağlamak için Java uygulamanızda aşağıdaki kodu kullanın.

## **Bir Alt Şeklin Ana Şeklini Alma**
Aspose.Diagram for Java, geliştiricilerin bir alt şeklin ana şeklini almasına olanak tanır.
### **Ebeveyn Şeklini Alın**
bu[Şekil](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape)class, üst şekli almak için ParentShape özelliğini sunar.
#### **Ebeveyn Şekli Programlama Örneği Alın**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RetrieveTheParentShape-RetrieveTheParentShape.java" >}}

