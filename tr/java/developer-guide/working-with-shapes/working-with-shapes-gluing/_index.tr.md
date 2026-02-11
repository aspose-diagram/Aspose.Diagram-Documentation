---
title: Shapes Gluing ile Çalışmak
type: docs
weight: 10
url: /tr/java/working-with-shapes-gluing/
---
## **Bağlayıcıları Belirli Bir Şekilde Yapıştırın**
[Ekle ve Bağla Visio Şekiller](/diagram/tr/java/add-and-connect-visio-shapes/) Microsoft Visio Aspose.Diagram for Java numaralı diyagramlarda bir şeklin nasıl eklenip diğer şekillere bağlanacağı anlatılmaktadır. Bu şekle yapıştırılmış konektörler de bulmak mümkündür.
### **Yapıştırılmış Şekiller Alma**
 Tarafından sunulan GluedShapes yöntemi[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)sınıf, bir şekle yapıştırılmış tüm bağlayıcıların kimliklerinin bir listesini veya söz konusu şekil bir bağlayıcı ise, bağlı olduğu şekillerin kimliklerini almak için kullanılabilir.[Şekil Koleksiyonu](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) class, kimliğine göre bir şekil bulmak için kullanılabilir.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir örnek dosya yükleyin.
1. Belirli bir şekle erişin.
1. Bu şekle yapıştırılmış tüm bağlayıcıların kimliklerinin bir listesini alın.
#### **Bağlayıcıları Yapıştırılmış Programlama Örneği Alın**
Aspose.Diagram for Java kullanarak bir şekle yapıştırılmış tüm konektörleri bulmak için Java uygulamanızda aşağıdaki kodu kullanın.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetGluedConnectors.class);   
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "RetrieveShapeInfo.vsd");
// get shape by an ID
Shape shape = diagram.getPages().get(0).getShapes().getShape(90);
// get all glued 1D shapes
long[] gluedShapeIds = shape.gluedShapes(GluedShapesFlags.GLUED_SHAPES_ALL_1_D, null, null);

// display shape ID and name
for (long id : gluedShapeIds)
{
    shape = diagram.getPages().get(0).getShapes().getShape(id);
    System.out.println("ID: " + shape.getID() + "\t\t Name: " + shape.getName());
}

{{< /highlight >}}
```
## **Yapıştırıcı Visio Şekilleri Bağlantı Noktasıyla Birlikte**
Aspose.Diagram for Java, geliştiricilerin bağlantı noktalarından şekilleri birbirine yapıştırmasına olanak tanır.
### **Tutkal Şekilleri**
 Tarafından sunulan GlueShapes yöntemi[Sayfa](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) sınıf kullanılabilir.

|<p>**Giriş diagram** </p><p>![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/Z69f4hg.png)</p>|<p>**Şekilleri yapıştırdıktan sonra diagram** </p><p>![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/5TJpDwc.png)</p>|
|:- |:- |
Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir örnek dosya yükleyin.
1. Şekilleri yapıştırın.
1. diagram'i kaydedin.
#### **Tutkal Visio Şekil Programlama Örneği**
Bağlantı noktalarından şekilleri yapıştırmak için Java uygulamanızda aşağıdaki kodu kullanın:

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GlueVisioShapes.class);
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.getPages().getPage("Page-1");
// set shape id
long shape1_ID = 7;
long shape2_ID = 494;
// Glue shapes
page.glueShapes(shape1_ID, ConnectionPointPlace.CENTER, shape2_ID);

// Save diagram
diagram.save(dataDir + "GlueVisioShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Kabın İçindeki Tutkal Şekilleri**
Aspose.Diagram for Java, geliştiricilerin grup şekillerini bir kapsayıcı içine yapıştırmalarına olanak tanır.
### **Tutkal Grubu Şekli**
Page sınıfı tarafından sunulan GlueShapesInContainer yöntemi kullanılabilir.

|<p>**Giriş diagram** </p><p>![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/HRRzIEh.png)</p>|<p>**Grup şekillerini yapıştırdıktan sonra diagram** </p><p>![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/YxCiOgU.png)</p>|
|:- |:- |
Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir örnek dosya yükleyin.
1. Grup şekillerini yapıştırın.
1. diagram'i kaydedin.
#### **Şekilleri Programlama Örneği İçinde Tutkalla**
Grup şeklini bir kabın içine yapıştırmak için Java uygulamanızda aşağıdaki kodu kullanın:

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GlueContainerShape.class);   
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.getPages().getPage("Page-1");

// The ID of shape which is glue from Aspose.Diagram.Shape.
long shapeFromId = 779;
// The location on the first connection index where to glue
int shapeToBeginConnectionIndex = 72;
// The location on the end connection index where to glue
int shapeToEndConnectionIndex = 73;
// The ID of shape where to glue to Aspose.Diagram.Shape.
long shapeToId = 743;

// Glue shapes in container
page.glueShapesInContainer(shapeFromId, shapeToBeginConnectionIndex, shapeToEndConnectionIndex, shapeToId);

// Glue shapes in container using connection name
// page.GlueShapesInContainer(fasId, "U05L", "U05R", cabinetId1);

// Save diagram
diagram.save(dataDir + "GlueContainerShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
