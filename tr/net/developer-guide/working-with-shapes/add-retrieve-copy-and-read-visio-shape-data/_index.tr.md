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

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-2");

// Add master with stencil file path and master name
string masterName = "Rectangle";
diagram.AddMaster(dataDir + "Basic Shapes.vss", masterName);
            
// Page indexing starts from 0
int PageIndex = 1;
double width = 2, height = 2, pinX = 4.25, pinY = 4.5;
// Add a new rectangle shape
long rectangleId = diagram.AddShape(pinX, pinY, width, height, masterName, PageIndex);
            
// Set shape properties 
Shape rectangle = page.Shapes.GetShape(rectangleId);
rectangle.XForm.PinX.Value = 5;
rectangle.XForm.PinY.Value = 5;
rectangle.Type = TypeValue.Shape;
rectangle.Text.Value.Add(new Txt("Aspose Diagram"));
rectangle.TextStyle = diagram.StyleSheets[3];
rectangle.Line.LineColor.Value = "#ff0000";
rectangle.Line.LineWeight.Value = 0.03;
rectangle.Line.Rounding.Value = 0.1;
rectangle.Fill.FillBkgnd.Value = "#ff00ff";
rectangle.Fill.FillForegnd.Value = "#ebf8df";

diagram.Save(dataDir + "AddShape_out.vsdx", SaveFileFormat.VSDX);
Console.WriteLine("Shape has been added.");

{{< /highlight >}}
```

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

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load diagram
Diagram vsdDiagram = new Diagram(dataDir + "RetrieveShapeInfo.vsd");

foreach (Aspose.Diagram.Shape shape in vsdDiagram.Pages[0].Shapes)
{
    // Display information about the shapes
    Console.WriteLine("\nShape ID : " + shape.ID);
    Console.WriteLine("Name : " + shape.Name);
    Console.WriteLine("Master Shape : " + shape.Master.Name);
}

{{< /highlight >}}
```
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
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();
            
// Load a source Visio
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");
            
// Initialize a new Visio
Diagram newDiagram = new Diagram();

// Add all masters from the source Visio diagram
MasterCollection originalMasters = srcVisio.Masters;
foreach (Master master in originalMasters)
    newDiagram.AddMaster(srcVisio, master.Name);

// Get the page object from the original diagram
Aspose.Diagram.Page SrcPage = srcVisio.Pages.GetPage("Page-1");
// Copy themes from the source diagram
newDiagram.CopyTheme(srcVisio);
// Copy pagesheet of the source Visio page
newDiagram.Pages[0].PageSheet.Copy(SrcPage.PageSheet);

// Copy shapes from the source Visio page
foreach (Aspose.Diagram.Shape shape in SrcPage.Shapes)
{
    newDiagram.Pages[0].Shapes.Add(shape);
}
// Save the new Visio
newDiagram.Save(dataDir + "CopyShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

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

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.Name == "Process1")
    {
        foreach (Prop property in shape.Props)
        {
            Console.WriteLine(property.Label.Value + ": " + property.Value.Val);
        }
        break;
    }
}

{{< /highlight >}}
```
### **Bir Şekil Özelliğini Ada Göre Okuma**
Aşağıdaki kod parçacığı, bir şekil özelliğini ada göre okur (özel özellik).
#### **Ada Göre Okuma Programlama Örneği**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.Name == "Process1")
    {
        Prop property = shape.Props.GetProp("Name1");
        Console.WriteLine(property.Label.Value + ": " + property.Value.Val);
    }
}

{{< /highlight >}}
```
### **InheritProps of Shape'i okuyun**
Aşağıdaki kod parçacığı, bir şeklin InheritProps'unu okur.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    foreach (Aspose.Diagram.Prop prop in shape.InheritProps)
    {
        Console.WriteLine(prop.Name);
        Console.WriteLine(prop.Label.Value);
        Console.WriteLine(prop.Prompt.Value);
        Console.WriteLine(prop.Type.Value.ToString());
        Console.WriteLine(prop.Value.Val);
        Console.WriteLine(prop.Format.Value);
    }
}

{{< /highlight >}}
```
## **Ekle ve Bağla Visio Şekiller**
 Aspose.Diagram for .NET, özelleştirilmiş şekiller eklemenizi ve bunları birbirine bağlamanızı sağlar.[oluşturduğunuz diyagramlar](https://products.aspose.com/diagram/net/).
### **Şekilleri Ekleme ve Birleştirme**
Aşağıdaki örneklerdeki kod, nasıl yapılacağını gösterir:

1. Bir diagram oluşturun.
1. Şekiller ekleyin ve özelleştirin (dikdörtgen, yıldız, altıgen).
1. Yıldız ve altıgen şekillerini dikdörtgene bağlayın.
1. diagram'i kaydedin.
#### **Şekilleri Ekleme ve Birleştirme Programlama Örneği**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_TechnicalArticles();

// Set license (you can add 10 shapes without setting a license)
// License lic = new License();
// Lic.SetLicense(dataDir + "Aspose.Total.lic");

// Load masters from any existing diagram, stencil or template
// And add in the new diagram
string visioStencil = dataDir + "AddConnectShapes.vss";

// Names of the masters present in the stencil
string rectangleMaster = @"Rectangle", starMaster = @"Star 7",
    hexagonMaster = @"Hexagon", connectorMaster = "Dynamic connector";

int pageNumber = 0;
double width = 2, height = 2, pinX = 4.25, pinY = 9.5;

// Create a new diagram
Diagram diagram = new Diagram(visioStencil);

// Add a new rectangle shape
long rectangleId = diagram.AddShape(
    pinX, pinY, width, height, rectangleMaster, pageNumber);

// Set the new shape's properties
Shape shape = diagram.Pages[pageNumber].Shapes.GetShape(rectangleId);
shape.Text.Value.Add(new Txt(@"Rectangle text."));
shape.Name = "Rectangle1";
shape.XForm.LocPinX.Ufe.F = "Width*0.5";
shape.XForm.LocPinY.Ufe.F = "Height*0.5";
shape.Line.LineColor.Value = "7";
shape.Line.LineWeight.Value = 0.03;
shape.Fill.FillBkgnd.Value = "1";
shape.Fill.FillForegnd.Value = "3";
shape.Fill.FillPattern.Value = 31;

// Add a new star shape
pinX = 2.0;
pinY = 4.5;
long starId = diagram.AddShape(
    pinX, pinY, width, height, starMaster, pageNumber);

// Set the star shape's properties
shape = diagram.Pages[pageNumber].Shapes.GetShape(starId);
shape.Text.Value.Add(new Txt(@"Star text."));
shape.Name = "Star1";
shape.XForm.LocPinX.Ufe.F = "Width*0.5";
shape.XForm.LocPinY.Ufe.F = "Height*0.5";
shape.Line.LineColor.Value = "#ff0000";
shape.Line.LineWeight.Value = 0.03;
shape.Fill.FillBkgnd.Value = "#ff00ff";
shape.Fill.FillForegnd.Value = "#0000ff";
shape.Fill.FillPattern.Value = 31;

// Add a new hexagon shape
pinX = 7.0;
long hexagonId = diagram.AddShape(
    pinX, pinY, width, height, hexagonMaster, pageNumber);

// Set the hexagon shape's properties
shape = diagram.Pages[pageNumber].Shapes.GetShape(hexagonId);
shape.Text.Value.Add(new Txt(@"Hexagon text."));
shape.Name = "Hexagon1";
shape.XForm.LocPinX.Ufe.F = "Width*0.5";
shape.XForm.LocPinY.Ufe.F = "Height*0.5";
shape.Line.LineWeight.Value = 0.03;
shape.Fill.FillPattern.Value = 31;

// Add master to dynamic connector from the stencil
diagram.AddMaster(visioStencil, connectorMaster);

// Connect rectangle and star shapes
Shape connector1 = new Shape();
long connecter1Id = diagram.AddShape(connector1, connectorMaster, 0);
diagram.Pages[0].ConnectShapesViaConnector(rectangleId, ConnectionPointPlace.Bottom,
    starId, ConnectionPointPlace.Top, connecter1Id);

// Connect rectangle and hexagon shapes
Shape connector2 = new Shape();
long connecter2Id = diagram.AddShape(connector2, connectorMaster, 0);
diagram.Pages[0].ConnectShapesViaConnector(rectangleId, ConnectionPointPlace.Bottom,
    hexagonId, ConnectionPointPlace.Left, connecter2Id);

// Save the diagram
diagram.Save(dataDir + "AddConnectShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
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
```
{{< highlight "csharp" >}}
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(13).Shapes.GetShape(2);
Shape parentShape = shape.ParentShape;
Console.WriteLine("Parent Shape's Properties:");
Console.WriteLine("Shape ID: " + parentShape.ID);
Console.WriteLine("Shape Name: " + parentShape.Name);
Console.WriteLine("Shape Type: " + parentShape.Type);
{{< /highlight >}}
```
