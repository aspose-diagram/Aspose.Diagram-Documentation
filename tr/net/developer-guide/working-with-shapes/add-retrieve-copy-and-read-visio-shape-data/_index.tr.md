---
title: Visio Şekil Verilerini Ekleme, Alma, Kopyalama ve Okuma
type: docs
weight: 10
url: /tr/net/add-retrieve-copy-and-read-visio-shape-data/
description: Bu bölüm, Aspose.Diagram ile bir şeklin nasıl ekleneceğini, şeklin özelliğinin nasıl ayarlanacağını veya bir şeklin nasıl kopyalanacağını açıklar.
---
## **Visio'de Yeni Şekil Ekleme**
Aspose.Diagram for .NET, Microsoft Visio diyagramlarını farklı şekillerde işlemenizi sağlar. Yapabileceğiniz şeylerden biri, diyagramlara yeni şekiller eklemektir. Aspose.Diagram for .NET, diagram'e yeni bir şekil eklemenizi sağlar. Eklenen şekil, Aspose.Diagram for .NET kullanılarak da özelleştirilebilir.

Bu konu, diagram'e yeni bir dikdörtgen şeklinin nasıl ekleneceğini açıklar.

Yeni şekiller oluşturmak için Aspose.Diagram for .NET API'i kullanın ve ardından bu şekilleri diagram'in şekil koleksiyonuna ekleyin.

Yeni bir şekil eklemek için:

1. **sayfayı bul** - Her Visio diagram, bir sayfa koleksiyonu içerir. Geliştiriciler, sayfayı sayfa kimliği veya Adına göre alabilir ve gerekli sayfayı[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page)sınıf nesnesi.
1. **Gerekli Master of a Shape'i ekleyin** - Her Visio diagram, bir usta koleksiyonu içerir. Geliştiriciler, mevcut şablon dosyasından (doğrudan yol veya dosya akışı yoluyla) bir Master (Kimlik veya Ada göre) ekleyebilir.
1. **Visio diagram'de şekil ekleyin** - Geliştiriciler, sayfa dizini (0'dan başlayarak), ana ad, PinX, PinY, yükseklik (isteğe bağlı) ve genişliğe (isteğe bağlı) göre Visio diagram'e yeni bir şekil yerleştirebilir.
1. **Şekil özelliklerini ayarla** - Diagram sınıfının AddShape yöntemi, şekil kimliğini döndürür. Geliştiriciler, bu kimliği kullanarak bir Visio diagram'den şekil alabilir ve ardından renk, konum, hizalama ve metin gibi özelliklerini ayarlayabilir.

|<p>**diagram girişi** </p><p>![yapılacaklar:resim_alternatif_Metin](add-retrieve-copy-and-read-visio-shape-data_1.png)</p>|<p>**Şekil eklenmiş diagram** </p><p>![yapılacaklar:resim_alternatif_Metin](add-retrieve-copy-and-read-visio-shape-data_2.png)</p>|
|:- |:- |
### **Programlama Örneği Ekle**
Aşağıdaki kod parçacığı, her bir adımın nasıl yapılacağını gösterir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-AddingNewShape-AddingNewShape.cs" >}}

{{% alert color="primary" %}}

 Soru ve önerilerinizi şu adrese bekliyoruz:[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Derhal cevap vereceğiz.

{{% /alert %}}
## **Şekil Bilgilerini Alma**
[Diyagramlarla Çalışmak](/diagram/tr/net/working-with-diagrams/)diyagramların nasıl oluşturulacağını, şekiller ve bağlayıcıların nasıl ekleneceğini ve ardından diagram gibi diagram öğeleri hakkında bilgilerin nasıl alınacağını açıklar.[sayfalar](/diagram/tr/net/retrieve-2c-get-2c-copy-and-insert-a-page/), [ustalar](https://docs.aspose.com/diagram/net/working-with-masters/), [konektörler](/diagram/tr/net/retrieving-connector-information/) ve[yazı tipleri](/diagram/tr/net/retrieving-font-information/). Bu makale, bir diagram'deki şekillerle ilgili bilgilerin nasıl alınacağını ele almaktadır.

diagram'deki her şeklin bir kimliği ve adı vardır. Kimlik, Visio ile programlama yaparken önemlidir: bir şekle erişmenin ana yöntemidir. Her şekil ayrıca hangi kalıptan (şablondan) yapıldığına dair bilgileri de tutar.

 A[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Visio çizimindeki bir nesnedir. Page sınıfı tarafından sunulan Shapes özelliği, Aspose.Diagram.Shape nesne koleksiyonunu destekler. Shapes özelliği, bir şekil hakkında bilgi almak için kullanılabilir.

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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-RetrieveShapeInfo-RetrieveShapeInfo.cs" >}}
## **Mevcut Bir Visio'den Şekilleri Kopyala**
Aspose.Diagram for .NET API, geliştiricilerin Visio kaynak sayfasındaki şekilleri yeni Visio diagram sayfasına kopyalamasına olanak tanır. Grup şekillerinin kopyalanmasını da destekler. Bu makalede, kaynak diagram sayfasındaki tüm şekillerin nasıl kopyalanacağı açıklanmaktadır.

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
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-CopyShape-CopyShape.cs" >}}

{{% alert color="primary" %}}

 Soru ve önerilerinizi şu adrese bekliyoruz:[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Derhal cevap vereceğiz.

{{% /alert %}}
## **Visio Shape'i başka bir Shape örneğine kopyalama**
Shape sınıfının Copy yöntemi, klonlamak için bir şekil örneği alır.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Shape newShape = new Shape();

// copy diagram

newShape.Copy(diagram.Pages[0].Shapes[0]);

newShape.ID = 3;

newShape.XForm.PinX.Value = 1;

newShape.XForm.PinY.Value = 1;

{{< /highlight >}}
## **Visio Şekil Verilerini Okuma**
 tarafından sergilenen Props koleksiyonu[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) sınıfı destekler[Aspose.Diagram.Prop](http://www.aspose.com/api/net/diagram/aspose.diagram/prop) nesne. Özellik, bir şeklin verilerini (özel özellikler) okumak için kullanılabilir.
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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-ReadAllShapeProps-ReadAllShapeProps.cs" >}}
### **Bir Şekil Özelliğini Ada Göre Okuma**
Aşağıdaki kod parçacığı, bir şekil özelliğini ada göre okur (özel özellik).
#### **Ada Göre Okuma Programlama Örneği**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-ReadShapePropByName-ReadShapePropByName.cs" >}}
### **InheritProps of Shape'i okuyun**
Aşağıdaki kod parçacığı, bir şeklin InheritProps'unu okur.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-InheritProps-InheritProps.cs" >}}
## **Ekle ve Bağla Visio Şekiller**
 Aspose.Diagram for .NET, özelleştirilmiş şekiller eklemenizi ve bunları birbirine bağlamanızı sağlar.[oluşturduğunuz diyagramlar](https://products.aspose.com/diagram/net/).
### **Şekilleri Ekleme ve Birleştirme**
Aşağıdaki örneklerdeki kod, nasıl yapılacağını gösterir:

1. Bir diagram oluşturun.
1. Şekiller ekleyin ve özelleştirin (dikdörtgen, yıldız, altıgen).
1. Yıldız ve altıgen şekillerini dikdörtgene bağlayın.
1. diagram'i kaydedin.
#### **Şekilleri Ekleme ve Birleştirme Programlama Örneği**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Technical-Articles-AddConnectShapes-AddConnectShapes.cs" >}}
## **Şekilleri bağlamak için Bağlantı dizinlerini kullanın**
Aspose.Diagram for .NET API zaten geliştiricilerin şekle yeni bağlantı noktaları eklemesine izin veriyor ve geliştiriciler artık bağlantı dizinlerini kullanarak şekilleri birbirine bağlayabiliyor.
### **Şekilleri bağlamak için Bağlantı dizinlerini kullanın**
Tarafından sunulan ConnectShapesViaConnectorIndex üyesi[Sayfa](https://reference.aspose.com/diagram/net/aspose.diagram/page)class, bağlantı dizinlerini kullanarak şekilleri bağlamak için kullanılabilir. Aşağıdaki kod, şekillerin nasıl bağlanacağını gösterir:

1. Yeni bir çizim başlatın.
1. Dört dikdörtgen şekli yerleştirin
1. Alt sınır çizgisinde üç bağlantı noktası olacak şekilde iki ek bağlantı noktası ekleyin
1. Her bir alt bağlantıdaki ilk şekli, dinamik bağlayıcılarla Üstteki diğer üç dikdörtgen şekle bağlayın
1. Çizimi kaydet
#### **Şekilleri bağlamak için bağlantı dizinlerini kullanın Programlama Örneği**
Aspose.Diagram for .NET API ile bağlantı dizinlerini kullanarak şekilleri bağlamak için .NET uygulamanızda aşağıdaki kodu kullanın.

**C#**

{{< highlight "java" >}}

 // initialize a new drawing

Diagram diagram = new Diagram();

// get page by index

Aspose.Diagram.Page page = diagram.Pages[0];

// add masters

string connectorMaster = "Dynamic connector", rectangle = "Rectangle";

int pageNumber = 0;

double width = 2, height = 2, pinX = 4.25, pinY = 9.5;

diagram.AddMaster(@"C:\temp\Basic Shapes.vss", rectangle);

diagram.AddMaster(@"C:\temp\Basic Shapes.vss", connectorMaster);

// add shapes

long shape1_ID = diagram.AddShape(4.5, 7, rectangle, pageNumber);

long shape2_ID = diagram.AddShape(2.25, 4.5, rectangle, pageNumber);

long shape3_ID = diagram.AddShape(4.5, 4.5, rectangle, pageNumber);

long shape4_ID = diagram.AddShape(6.75, 4.5, rectangle, pageNumber);

// get shapes by ID

Aspose.Diagram.Shape shape1 = page.Shapes.GetShape(shape1_ID);

Aspose.Diagram.Shape shape2 = page.Shapes.GetShape(shape2_ID);

Aspose.Diagram.Shape shape3 = page.Shapes.GetShape(shape3_ID);

Aspose.Diagram.Shape shape4 = page.Shapes.GetShape(shape4_ID);

// add two more connection points

Connection connection1 = new Connection();

connection1.X.Ufe.F = "Width*0.33";

connection1.Y.Ufe.F = "Height*0";

Connection connection3 = new Connection();

connection3.X.Ufe.F = "Width*0.66";

connection3.Y.Ufe.F = "Height*0";

shape1.Connections.Add(connection1);

shape1.Connections.Add(connection3);



// add connector shapes

Aspose.Diagram.Shape connector1 = new Aspose.Diagram.Shape();

Aspose.Diagram.Shape connector2 = new Aspose.Diagram.Shape();

Aspose.Diagram.Shape connector3 = new Aspose.Diagram.Shape();

long connecter1Id = diagram.AddShape(connector1, connectorMaster, 0);

long connecter2Id = diagram.AddShape(connector2, connectorMaster, 0);

long connecter3Id = diagram.AddShape(connector3, connectorMaster, 0);

// connect shapes by index of conneecting points

page.ConnectShapesViaConnectorIndex(shape1.ID, 6, shape2.ID, 3, connecter1Id);

page.ConnectShapesViaConnectorIndex(shape1.ID, 1, shape3.ID, 3, connecter2Id);

page.ConnectShapesViaConnectorIndex(shape1.ID, 7, shape4.ID, 3, connecter3Id);

// save drawing

diagram.Save(@"C:\temp\Drawing1_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Bir Alt Şeklin Ana Şeklini Alma**
Aspose.Diagram for .NET, geliştiricilerin bir alt şeklin ana şeklini almasına olanak tanır.
### **Ebeveyn Şeklini Alın**
bu[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)class, üst şekli almak için ParentShape özelliğini sunar.
#### **Ebeveyn Şekli Programlama Örneği Alın**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-RetrieveTheParentShape-RetrieveTheParentShape.cs" >}}
