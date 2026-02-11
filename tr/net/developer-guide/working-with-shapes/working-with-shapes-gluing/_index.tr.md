---
title: Shapes Gluing ile Çalışmak
type: docs
weight: 40
url: /tr/net/working-with-shapes-gluing/
description: Bu bölümde, Aspose.Diagram ile belirli bir şekle yapıştırılan şekillerin nasıl elde edileceği açıklanmaktadır.
---
## **Bağlayıcıları Belirli Bir Şekilde Yapıştırın**
[Ekle ve Bağla Visio Şekiller](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) Microsoft Visio Aspose.Diagram for .NET numaralı diyagramlarda bir şeklin nasıl eklenip diğer şekillere bağlanacağı anlatılmaktadır. Bu şekle yapıştırılmış konektörler de bulmak mümkündür.
### **Yapıştırılmış Şekiller Alma**
 Tarafından sunulan GluedShapes yöntemi[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)sınıf, bir şekle yapıştırılmış tüm bağlayıcıların kimliklerinin bir listesini veya söz konusu şekil bir bağlayıcı ise, bağlı olduğu şekillerin kimliklerini almak için kullanılabilir.[Şekil Koleksiyonu](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) class, kimliğine göre bir şekil bulmak için kullanılabilir.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir örnek dosya yükleyin.
1. Belirli bir şekle erişin.
1. Bu şekle yapıştırılmış tüm bağlayıcıların kimliklerinin bir listesini alın.
#### **Bağlayıcıları Yapıştırılmış Programlama Örneği Alın**
Aspose.Diagram for .NET kullanarak bir şekle yapıştırılmış tüm konektörleri bulmak için .NET uygulamanızda aşağıdaki kodu kullanın.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "RetrieveShapeInfo.vsd");
// Get shape by an ID
Shape shape = diagram.Pages[0].Shapes.GetShape(90);
// Get all glued 1D shapes
long[] gluedShapeIds = shape.GluedShapes(GluedShapesFlags.GluedShapesAll1D, null, null);

// Display shape ID and name
foreach (long id in gluedShapeIds)
{
    shape = diagram.Pages[0].Shapes.GetShape(id);
    Console.WriteLine("ID: " + shape.ID + "\t\t Name: " + shape.Name);
}

{{< /highlight >}}

## **Yapıştırıcı Visio Şekilleri Bağlantı Noktasıyla Birlikte**
Aspose.Diagram for .NET, geliştiricilerin bağlantı noktalarından şekilleri birbirine yapıştırmasına olanak tanır.
### **Tutkal Şekilleri**
 Tarafından sunulan GlueShapes yöntemi[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page) sınıf kullanılabilir.

|<p>**Giriş diagram** </p><p>![yapılacaklar:resim_alternatif_Metin](working-with-shapes-gluing_1.png)</p>|<p>**Şekilleri yapıştırdıktan sonra diagram** </p><p>![yapılacaklar:resim_alternatif_Metin](working-with-shapes-gluing_2.png)</p>|
|:- |:- |
Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir örnek dosya yükleyin.
1. Şekilleri yapıştırın.
1. diagram'i kaydedin.
#### **Tutkal Visio Şekil Programlama Örneği**
Bağlantı noktalarından şekilleri yapıştırmak için .NET uygulamanızda aşağıdaki kodu kullanın:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.Pages.GetPage("Page-1");
// Set shape id
long shape1_ID = 7;
long shape2_ID = 494;
// Glue shapes
page.GlueShapes(shape1_ID, Aspose.Diagram.Manipulation.ConnectionPointPlace.Center, shape2_ID);

// Save diagram
diagram.Save(dataDir + "GlueVisioShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Kabın İçindeki Tutkal Şekilleri**
Aspose.Diagram for .NET, geliştiricilerin grup şekillerini bir kapsayıcı içine yapıştırmalarına olanak tanır.
### **Tutkal Grubu Şekli**
 Tarafından sunulan GlueShapesInContainer yöntemi[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page) sınıf kullanılabilir.

|<p>**Giriş diagram** </p><p>![yapılacaklar:resim_alternatif_Metin](working-with-shapes-gluing_3.png)</p>|<p>**Grup şekillerini yapıştırdıktan sonra diagram** </p><p>![yapılacaklar:resim_alternatif_Metin](working-with-shapes-gluing_4.png)</p>|
|:- |:- |
Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir örnek dosya yükleyin.
1. Grup şekillerini yapıştırın.
1. diagram'i kaydedin.
#### **Şekilleri Programlama Örneği İçinde Tutkalla**
Grup şeklini bir kabın içine yapıştırmak için .NET uygulamanızda aşağıdaki kodu kullanın:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.Pages.GetPage("Page-1");

// The ID of shape which is glue from Aspose.Diagram.Shape.
long shapeFromId = 779;
// The location on the first connection index where to glue
int shapeToBeginConnectionIndex = 72;
// The location on the end connection index where to glue
int shapeToEndConnectionIndex = 73;
// The ID of shape where to glue to Aspose.Diagram.Shape.
long shapeToId = 743;

// Glue shapes in container
page.GlueShapesInContainer(shapeFromId, shapeToBeginConnectionIndex, shapeToEndConnectionIndex, shapeToId);

// Glue shapes in container using connection name
// Page.GlueShapesInContainer(fasId, "U05L", "U05R", cabinetId1);

// Save diagram
diagram.Save(dataDir + "GlueContainerShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

