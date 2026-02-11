---
title: Döndürün, Konumu Değiştirin ve Alt Şekilleri Bağlayın
type: docs
weight: 60
url: /tr/java/rotate-change-the-position-and-connect-sub-shapes/
---
## **Bir Şekli Uygun Açıyla Döndürün**
 Aspose.Diagram for Java, bir şekli herhangi bir açıda döndürmenizi sağlar. Tarafından sunulan SetAngle yöntemi[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) sınıf, bir şekli istenen herhangi bir açıda döndürmek için kullanılabilir. Açı olarak tek bir parametre alır.
### **Şekil Programlama Örneği Döndürme**
Aspose.Diagram for Java kullanarak bir şekli döndürmek için Java uygulamanızda aşağıdaki kodu kullanın.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RotateVisioShape.class); 
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");
// get shape by id
Shape shape = page.getShapes().getShape(16);

// Add a shape and set the angle
shape.setAngle(190);

// Save diagram
diagram.save(dataDir + "RotateVisioShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Bir Şeklin Konumunu Değiştirme**
Şekil Sınıfı, bir şeklin konumunu değiştirmenize olanak tanır. Şekil farklı bir konuma taşındığında bağlayıcı çizgi otomatik olarak ayarlanır.

Shape sınıfı tarafından sunulan Move ve MoveTo yöntemleri, bir grubun parçası olarak veya değil, bir şeklin konumunu değiştirmeyi destekler.
Bu makaledeki kod örnekleri, sayfada bir şekli hareket ettirir.
**Giriş diagram** 

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/cThgWnB.png)


**Şekil taşındıktan sonra diagram** 

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/Q3QByqe.png)

Bir şekli taşıma işlemi:

1. diagram yükleyin.
1. Belirli bir şekil bulun.
1. Şekli farklı bir konuma taşı
1. diagram'i kaydedin.
### **Konum Değiştirme Programlama Örneği**
Aşağıdaki kod parçacığı, şeklin nasıl taşınacağını gösterir. Kod, ada göre bir Visio sayfasını ve ID 16'ya göre şekli alır ve konumunu hareket ettirir.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(MoveVisioShape.class);  
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");
// get shape by id
Shape shape = page.getShapes().getShape(16);
// move shape from its position, it adds values in coordinates
shape.move(1, 1);

// save diagram
diagram.save(dataDir + "MoveVisioShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Grupların Alt Şekillerini Bağlayın**
Bu konuda, Aspose.Diagram for Java kullanılarak Microsoft Visio diyagramlarında iki farklı grup şeklinin iki alt şeklinin nasıl birleştirileceği açıklanmaktadır.

 Tarafından sunulan ConnectShapesViaConnector yöntemi[Sayfa](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) class, şekilleri kimliklerine göre bağlamak için kullanılabilir. Tarafından sunulan AddShape yöntemi[Diagram](https://reference.aspose.com/diagram/java)sınıf, bir şekil eklemek için kullanılabilir.

|<p>**diagram girişi** </p><p>![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/74rDby5.png)</p>|<p>**Alt şekillerin bağlanmasından sonra diagram** </p><p>![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/c387dZJ.png)</p>|
|:- |:- |
Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir örnek dosya yükleyin.
1. Belirli bir sayfaya erişin.
1. Seçilen sayfaya dinamik bağlayıcı şekli ekleyin.
1. Alt şekilleri birleştir
### **Alt Şekilleri Programlama Örneği Bağlayın**
Java for Java kullanarak iki farklı grup şeklinin alt şekillerini bağlamak için Java uygulamanızda aşağıdaki kodu kullanın.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ConnectVisioSubShapes.class);   
// set sub shape ids
long shapeFromId = 2;
long shapeToId = 4;

// load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// access a particular page
Page page = diagram.getPages().getPage("Page-3");
       
// initialize connector shape
Shape shape = new Shape();
shape.getLine().getEndArrow().setValue(4);
shape.getLine().getLineWeight().setValue(0.01388);

// add shape
long connecter1Id = diagram.addShape(shape, "Dynamic connector", page.getID());
// connect sub-shapes
page.connectShapesViaConnector(shapeFromId, ConnectionPointPlace.RIGHT, shapeToId, ConnectionPointPlace.LEFT, connecter1Id);
// save Visio drawing
diagram.save(dataDir + "ConnectVisioSubShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Şekilleri Belirli Bir Şekle Bağlayın**
[Ekle ve Bağla Visio Şekiller](/diagram/tr/java/add-and-connect-visio-shapes/) Microsoft Visio diyagramlarında Aspose.Diagram for Java kullanılarak bir şeklin nasıl eklenip diğer şekillere bağlanacağı anlatılmaktadır. Belirli bir şekle bağlı şekiller bulmak da mümkündür.

 Tarafından sunulan ConnectedShapes yöntemi[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class, bir şekle bağlı şekillerin kimliklerini almak için kullanılabilir. Tarafından sunulan GetShape yöntemi[Şekil Koleksiyonu](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) class, kimliğine göre bir şekil bulmak için kullanılabilir.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir örnek dosya yükleyin.
1. Belirli bir şekle erişin.
1. Seçilen şekle bağlı tüm şekillerin adlarını alın.
### **Shapes Programlama Örneği Alın**
Aspose.Diagram for Java kullanarak belirli bir şekle bağlı tüm şekilleri bulmak için Java uygulamanızda aşağıdaki kodu kullanın.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetAllConnectedShapes.class);
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get shape by id
Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(16);
// get connected shapes
long[] connectedShapeIds = shape.connectedShapes(ConnectedShapesFlags.CONNECTED_SHAPES_ALL_NODES, null);

for (long id : connectedShapeIds)
{
    shape = diagram.getPages().getPage("Page-3").getShapes().getShape(id);
    System.out.println("ID: " + shape.getID() + "\t\t Name: " + shape.getName());
}

{{< /highlight >}}

