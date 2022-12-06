---
title: Visio Şekil Verisi ile Çalışma
type: docs
weight: 30
url: /tr/java/working-with-visio-shape-data/
---
## **Visio'de Yeni Şekil Ekleme**
Aspose.Diagram for Java, Microsoft Visio diyagramlarını farklı şekillerde işlemenizi sağlar. Yapabileceğiniz şeylerden biri, diyagramlara yeni şekiller eklemektir. Aspose.Diagram for Java, diagram'e yeni bir şekil eklemenizi sağlar. Eklenen şekil, Aspose.Diagram for Java kullanılarak da özelleştirilebilir.

Bu konu, diagram'e yeni bir dikdörtgen şeklinin nasıl ekleneceğini açıklar.

Yeni şekiller oluşturmak için Aspose.Diagram for Java'in API'ini kullanın ve ardından bu şekilleri bir diagram'in şekil koleksiyonuna ekleyin.

Yeni bir şekil eklemek için:

1. **sayfayı bul** - Her Visio diagram, bir sayfa koleksiyonu içerir. Geliştiriciler, sayfayı sayfa kimliği veya Adına göre alabilir ve gerekli sayfayı[Sayfa](https://reference.aspose.com/diagram//java/com.aspose.diagram/page)sınıf nesnesi.
1. **Gerekli Master of a Shape'i ekleyin** - Her Visio diagram, bir usta koleksiyonu içerir. Geliştiriciler, mevcut şablon dosyasından (doğrudan yol veya dosya akışı yoluyla) bir Master (Kimlik veya Ada göre) ekleyebilir.
1. **Visio diagram'de şekil ekleyin** - Geliştiriciler, sayfa dizini (0'dan başlayarak), ana ad, PinX, PinY, yükseklik (isteğe bağlı) ve genişliğe (isteğe bağlı) göre Visio diagram'e yeni bir şekil yerleştirebilir.
1. **Şekil özelliklerini ayarla** - Diagram sınıfının AddShape yöntemi, şekil kimliğini döndürür. Geliştiriciler, bu kimliği kullanarak bir Visio diagram'den şekil alabilir ve ardından renk, konum, hizalama ve metin gibi özelliklerini ayarlayabilir.

|<p>**diagram girişi** </p><p>![yapılacaklar:resim_alternatif_Metin](working-with-visio-shape-data_1.png)</p>|<p>**Şekil eklenmiş diagram** </p><p>![yapılacaklar:resim_alternatif_Metin](working-with-visio-shape-data_2.png)</p>|
|:- |:- |
### **Programlama Örneği Ekle**
Aşağıdaki kod parçacığı, her bir adımın nasıl yapılacağını gösterir.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-AddingNewShape-AddingNewShape.java" >}}

{{% alert color="primary" %}}

 Soru ve önerilerinizi şu adrese bekliyoruz:[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Derhal cevap vereceğiz.

{{% /alert %}}
## **Şekil Bilgilerini Alma**
[Diyagramlarla Çalışmak](/diagram/tr/java/working-with-diagrams/)diyagramların nasıl oluşturulacağını, şekiller ve bağlayıcıların nasıl ekleneceğini ve ardından diagram gibi diagram öğeleri hakkında bilgilerin nasıl alınacağını açıklar.[sayfalar](/diagram/tr/java/retrieve-get-copy-and-insert-a-page/), [ustalar](/diagram/tr/java/working-with-masters/) , konektörler ve[yazı tipleri](/diagram/tr/java/aspose-diagram-font-operations/). Bu makale, bir diagram'deki şekillerle ilgili bilgilerin nasıl alınacağını ele almaktadır.

diagram'deki her şeklin bir kimliği ve adı vardır. Kimlik, Visio ile programlama yaparken önemlidir: bir şekle erişmenin ana yöntemidir. Her şekil ayrıca hangi kalıptan (şablondan) yapıldığına dair bilgileri de tutar.

 A[Şekil](https://reference.aspose.com/diagram//java/com.aspose.diagram/shape) Visio çizimindeki bir nesnedir. Page sınıfı tarafından sunulan Shapes özelliği, Aspose.Diagram.Shape nesne koleksiyonunu destekler. Shapes özelliği, bir şekil hakkında bilgi almak için kullanılabilir.

Örneğin aşağıdaki konsol penceresinde, dört şekil içeren bir diagram için bilgi çıktısını görebilirsiniz: iki sonlandırıcı, bir işlem ve bir dinamik bağlayıcı. Her birinin benzersiz bir kimliği ve ana (kalıp) şeklinin adı vardır.

**Şekil bilgilerini gösteren bir konsol penceresi**

![yapılacaklar:resim_alternatif_Metin](working-with-visio-shape-data_3.png)

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
Shape sınıfının kopyalama yöntemi, klonlamak için bir şekil örneği alır.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Shape newShape = new Shape();

// copy diagram

newShape.copy(diagram.getPages().get(0).getShapes().get(0));

newShape.setID(3);

newShape.getXForm().getPinX().setValue(1);

newShape.getXForm().getPinY().setValue(1);

{{< /highlight >}}
## **Visio Şekil Verilerini Okuma**
 Shape sınıfı tarafından sunulan Props koleksiyonu,[Aspose.Diagram.Prop](https://reference.aspose.com/diagram//java/com.aspose.diagram/prop) nesne. Özellik, bir şeklin verilerini (özel özellikler) okumak için kullanılabilir.
### **Tüm Şekil Özelliklerini Oku**
Microsoft Visio'de özel özellikleri tanımlamak için:

1. diagram'de bir şekle sağ tıklayın.
1.  Seçme**Veri** , sonra**Şekil Verisi** menüden.
 Varolan tüm özellikler iletişim kutusunda listelenir.

|**Microsoft Visio'de görüldüğü gibi bir şeklin verileri.**|** |
|:- |:- |
|![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/2loM7b0.png)||


|**Şekil verisi çıktısını gösteren bir konsol penceresi.**|** |
|:- |:- |
|![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/kmAKNrx.png)||
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
Page sınıfı tarafından sunulan connectShapesViaConnectorIndex üyesi, bağlantı dizinlerini kullanarak şekilleri bağlamak için kullanılabilir. Aşağıdaki kod, şekillerin nasıl bağlanacağını gösterir:

1. Yeni bir çizim başlatın.
1. Dört dikdörtgen şekli yerleştirin
1. Alt sınır çizgisinde üç bağlantı noktası olacak şekilde iki ek bağlantı noktası ekleyin
1. Her bir alt bağlantıdaki ilk şekli, dinamik bağlayıcılarla Üstteki diğer üç dikdörtgen şekle bağlayın
1. Çizimi kaydet
#### **Şekilleri bağlamak için bağlantı dizinlerini kullanın Programlama Örneği**
Aspose.Diagram for Java API ile bağlantı dizinlerini kullanarak şekilleri bağlamak için Java uygulamanızda aşağıdaki kodu kullanın.

**Java**

{{< highlight "java" >}}

 // initialize a new drawing

Diagram diagram = new Diagram();

// get page by index

Page page = diagram.getPages().get(0);

// add masters

String connectorMaster = "Dynamic connector", rectangle = "Rectangle";

int pageNumber = 0;

double width = 2, height = 2, pinX = 4.25, pinY = 9.5;

diagram.addMaster("C:\\temp\\Basic Shapes.vss", rectangle);

diagram.addMaster("C:\\temp\\Basic Shapes.vss", connectorMaster);

// add shapes

long shape1_ID = diagram.addShape(4.5, 7, rectangle, pageNumber);

long shape2_ID = diagram.addShape(2.25, 4.5, rectangle, pageNumber);

long shape3_ID = diagram.addShape(4.5, 4.5, rectangle, pageNumber);

long shape4_ID = diagram.addShape(6.75, 4.5, rectangle, pageNumber);

// get shapes by ID

Shape shape1 = page.getShapes().getShape(shape1_ID);

Shape shape2 = page.getShapes().getShape(shape2_ID);

Shape shape3 = page.getShapes().getShape(shape3_ID);

Shape shape4 = page.getShapes().getShape(shape4_ID);

// add two more connection points

Connection connection1 = new Connection();

connection1.getX().getUfe().setF("Width*0.33");

connection1.getY().getUfe().setF("Height*0");

Connection connection3 = new Connection();

connection3.getX().getUfe().setF("Width*0.66");

connection3.getY().getUfe().setF("Height*0");

shape1.getConnections().add(connection1);

shape1.getConnections().add(connection3);



// add connector shapes

Shape connector1 = new Shape();

Shape connector2 = new Shape();

Shape connector3 = new Shape();

long connecter1Id = diagram.addShape(connector1, connectorMaster, 0);

long connecter2Id = diagram.addShape(connector2, connectorMaster, 0);

long connecter3Id = diagram.addShape(connector3, connectorMaster, 0);

// connect shapes by index of conneecting points

page.connectShapesViaConnectorIndex(shape1.getID(), 6, shape2.getID(), 3, connecter1Id);

page.connectShapesViaConnectorIndex(shape1.getID(), 1, shape3.getID(), 3, connecter2Id);

page.connectShapesViaConnectorIndex(shape1.getID(), 7, shape4.getID(), 3, connecter3Id);

// save drawing

diagram.save("C:\\temp\\Drawing1_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Bir Alt Şeklin Ana Şeklini Alma**
Aspose.Diagram for Java, geliştiricilerin bir alt şeklin ana şeklini almasına olanak tanır.
### **Ebeveyn Şeklini Alın**
Shape sınıfı, ana şekli almak için getParentShape özelliğini sunar.
#### **Ebeveyn Şekli Programlama Örneği Alın**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RetrieveTheParentShape-RetrieveTheParentShape.java" >}}
