---
title: Döndürün, Konumu Değiştirin ve Alt Şekilleri Bağlayın
type: docs
weight: 30
url: /tr/net/rotate-change-the-position-and-connect-sub-shapes/
description: Bu bölümde bir visio şeklinin Aspose.Diagram ile nasıl döndürüleceği açıklanmaktadır.
---
## **Bir Şekli Uygun Açıyla Döndürün**
 Aspose.Diagram for .NET, bir şekli herhangi bir açıda döndürmenizi sağlar. Tarafından sunulan SetAngle yöntemi[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) sınıf, bir şekli istenen herhangi bir açıda döndürmek için kullanılabilir. Açı olarak tek bir parametre alır.
### **Şekil Programlama Örneği Döndürme**
Aspose.Diagram for .NET kullanarak bir şekli döndürmek için .NET uygulamanızda aşağıdaki kodu kullanın.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");
// Get shape by id
Shape shape = page.Shapes.GetShape(16);

// Add a shape and set the angle
shape.SetAngle(190);

// Save diagram
diagram.Save(dataDir + "RotateVisioShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Bir Şeklin Konumunu Değiştirme**
 bu[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Class, bir şeklin konumunu değiştirmenizi sağlar. Şekil farklı bir konuma taşındığında bağlayıcı çizgi otomatik olarak ayarlanır. Tarafından sunulan Move ve MoveTo yöntemleri[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) sınıf, bir grubun parçası olarak veya değil, bir şeklin konumunu değiştirmeyi destekler. Bu makaledeki kod örnekleri, sayfada bir şekli hareket ettirir.

Bir şekli taşıma işlemi:

1. diagram yükleyin.
1. Belirli bir şekil bulun.
1. Şekli farklı bir konuma taşı
1. diagram'i kaydedin.
### **Konum Değiştirme Programlama Örneği**
Aşağıdaki kod parçacığı, şeklin nasıl taşınacağını gösterir. Kod, ada göre bir Visio sayfasını ve ID 16'ya göre şekli alır ve konumunu hareket ettirir.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");
// Get shape by id
Shape shape = page.Shapes.GetShape(16);
// Move shape from its position, it adds values in coordinates
shape.Move(1, 1);

// Save diagram
diagram.Save(dataDir + "MoveVisioShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Grupların Alt Şekillerini Bağlayın**
 Bu konuda, Microsoft Visio diyagramlarında Aspose.Diagram for .NET kullanılarak iki farklı grup şeklinin iki alt şeklinin nasıl birleştirileceği açıklanmaktadır.[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class, şekilleri kimliklerine göre bağlamak için kullanılabilir. Tarafından sunulan AddShape yöntemi[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)sınıf, bir şekil eklemek için kullanılabilir.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir örnek dosya yükleyin.
1. Belirli bir sayfaya erişin.
1. Seçilen sayfaya dinamik bağlayıcı şekli ekleyin.
1. Alt şekilleri birleştir
### **Alt Şekilleri Programlama Örneği Bağlayın**
.NET for .NET kullanarak iki farklı grup şeklinin alt şekillerini bağlamak için .NET uygulamanızda aşağıdaki kodu kullanın.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Set sub shape ids
long shapeFromId = 2;
long shapeToId = 4;

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Access a particular page
Page page = diagram.Pages.GetPage("Page-3");
           
// Initialize connector shape
Shape shape = new Shape();
shape.Line.EndArrow.Value = 4;
shape.Line.LineWeight.Value = 0.01388;

// Add shape
long connecter1Id = diagram.AddShape(shape, "Dynamic connector", page.ID);
// Connect sub-shapes
page.ConnectShapesViaConnector(shapeFromId, ConnectionPointPlace.Right, shapeToId, ConnectionPointPlace.Left, connecter1Id);
// Save Visio drawing
diagram.Save(dataDir + "ConnectVisioSubShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Şekilleri Belirli Bir Şekle Bağlayın**
[Ekle ve Bağla Visio Şekiller](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) Microsoft Visio diyagramlarında Aspose.Diagram for .NET kullanılarak bir şeklin nasıl eklenip diğer şekillere bağlanacağı anlatılmaktadır. Belirli bir şekle bağlı şekiller bulmak da mümkündür.

 Tarafından sunulan ConnectedShapes yöntemi[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, bir şekle bağlı şekillerin kimliklerini almak için kullanılabilir. Tarafından sunulan GetShape yöntemi[Şekil Koleksiyonu](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) class, kimliğine göre bir şekil bulmak için kullanılabilir.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir örnek dosya yükleyin.
1. Belirli bir şekle erişin.
1. Seçilen şekle bağlı tüm şekillerin adlarını alın.
### **Shapes Programlama Örneği Alın**
Aspose.Diagram for .NET kullanarak belirli bir şekle bağlı tüm şekilleri bulmak için .NET uygulamanızda aşağıdaki kodu kullanın.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get shape by id
Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(16);
// Get connected shapes
long[] connectedShapeIds = shape.ConnectedShapes(ConnectedShapesFlags.ConnectedShapesAllNodes, null);

foreach (long id in connectedShapeIds)
{
    shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(id);
    Console.WriteLine("ID: " + shape.ID + "\t\t Name: " + shape.Name);
}

{{< /highlight >}}

