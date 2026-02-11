---
title: Şekilleri Gruplandırın, Dönüştürün ve Doğrulayın
type: docs
weight: 80
url: /tr/net/group-convert-and-verify-shapes/
description: Bu bölümde şekillerin Aspose.Diagram ile nasıl gruplandırılacağı açıklanmaktadır.
---
## **Visio Çiziminde Birden Fazla Şekli Birlikte Gruplandırın**
Aspose.Diagram API, geliştiricilerin şekilleri bir arada gruplandırmasına ve hepsini aynı anda taşımasına olanak tanır. Bir gruptaki her şekil benzersiz bir kimliğe sahiptir ve kendi özelliklerine sahiptir. Bir şekil grubunun biçimlendirmesini değiştirdiğimizde, her şekle yeni özellik atar.
### **Şekiller Nasıl Gruplandırılır?**
 tarafından sunulan Grup yöntemi[Şekil Koleksiyonu](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) class, şekilleri birlikte gruplandırmak için kullanılabilir.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir numune yükleyin diagram.
1. şekillerin bir dizisini başlattı
1. kimliğe göre belirli bir şekil elde edin.
1. kimliğe göre başka bir özel şekil elde edin.
1. diziye şekiller atayın.
1. Group yöntemini çağırarak şekilleri gruplandırın.
1. kaydet diagram
#### **Grup Şekilleri Programlama Örneği**
Aspose.Diagram for .NET API'i kullanarak şekilleri gruplandırmak için .NET uygulamanızda aşağıdaki kodu kullanın.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

// Initialize an array of shapes
Aspose.Diagram.Shape[] ss = new Aspose.Diagram.Shape[3];

// Extract and assign shapes to the array
ss[0] = page.Shapes.GetShape(15);
ss[1] = page.Shapes.GetShape(16);
ss[2] = page.Shapes.GetShape(17);

// Mark array shapes as group
page.Shapes.Group(ss);

// Save visio diagram
diagram.Save(dataDir + "GroupShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Visio Şeklini Diğer Dosya Biçimlerine Dönüştürme**
Aspose.Diagram for .NET API, geliştiricilerin tek bir Visio şeklini desteklenen diğer herhangi bir dosya biçimine dönüştürmesine olanak tanır. Bu yazıda, diğer tüm Visio şekillerini sayfadan kaldırıyoruz ve sayfa ayarını kaynak Şekil boyutuna göre özelleştiriyoruz.
### **Belirli Bir Şekli Dönüştürme Visio**
 Geliştiriciler, bir Visio şeklini şu şekilde PDF, HTML, Image, SVG ve SWF'e dönüştürebilir.**Visio kaydetme seçeneklerini belirleme**.
Bu örnek kod aşağıdaki gibi çalışır:

1. Bir kaynak yükleyin Visio.
1. Belirli bir sayfa alın.
1. Arka plan sayfasını kaldırın.
1. Kimlikleri ve adları tutan tüm şekillerden oluşan bir karma tablo oluşturun.
1. Hash tablosunu yineleyin
1. Belirli bir şekil dışında tüm şekilleri Visio sayfasından kaldırın.
1. Sayfa boyutunu ayarlayın.
1. Visio sayfasını desteklenen herhangi bir dosya biçiminde kaydedin.
#### **Şekil Programlama Örneği Dönüştür**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");

double shapeWidth = 0;
double shapeHeight = 0;

// Get Visio page
Aspose.Diagram.Page srcPage = srcVisio.Pages.GetPage("Page-3");
// Remove background page
srcPage.BackPage = null;

// Get hash table of shapes, it holds id and name
Hashtable remShapes = new Hashtable();
// Hashtable<Long, String> remShapes = new Hashtable<Long, String>();
foreach (Aspose.Diagram.Shape shape in srcPage.Shapes)
    // For the normal shape
    remShapes.Add(shape.ID, shape.Name);

// Iterate through the hash table
foreach (DictionaryEntry shapeEntry in remShapes)
{
    long key = (long)shapeEntry.Key;
    string val = (string)shapeEntry.Value;
    Aspose.Diagram.Shape shape = srcPage.Shapes.GetShape(key);
    // Check of the shape name
    if (val.Equals("GroupShape1"))
    {
        // Move shape to the origin corner
        shapeWidth = shape.XForm.Width.Value;
        shapeHeight = shape.XForm.Height.Value;
        shape.MoveTo(shapeWidth * 0.5, shapeHeight * 0.5);
        // Trim page size
        srcPage.PageSheet.PageProps.PageWidth.Value = shapeWidth;
        srcPage.PageSheet.PageProps.PageHeight.Value = shapeHeight;
    }
    else
    {
        // Remove shape from the Visio page and hash table
        srcPage.Shapes.Remove(shape);
    }
}
remShapes.Clear();

// Specify saving options
Aspose.Diagram.Saving.PdfSaveOptions opts = new Aspose.Diagram.Saving.PdfSaveOptions();
// Set page count to save
opts.PageCount = 1;
// Set starting index of the page
opts.PageIndex = 1;
// Save it
srcVisio.Save(dataDir + "SaveVisioShapeInOtherFormats_out.pdf", opts);

{{< /highlight >}}

### **Visio Şeklini PDF'e dönüştür**
Shape sınıfının ToPdf yöntemi, bir şekli PDF biçimine dönüştürmeye olanak tanır.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Visio Şeklini HTML'e dönüştür**
Shape sınıfının ToHTML yöntemi, bir şeklin HTML biçimine dönüştürülmesine izin verir.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}
## **İki Visio Şeklin Bağlantılı veya Yapıştırılmış Olduğunu Doğrulayın**
 Aspose.Diagram for .NET API, geliştiricilerin iki Visio şeklinin yapıştırıldığını veya bağlantılı olduğunu doğrulamasına olanak tanır. Daha önce, bu yardım konularında iki şekli nasıl birleştirebileceğimizi veya yapıştırabileceğimizi gördük:[Ekle ve Bağla Visio Şekiller](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) ve[Kabın İçindeki Tutkal Şekilleri](/diagram/tr/net/working-with-shapes-gluing/).
### **Bağlı veya Yapıştırılmış Şekillerin Doğrulanması**
 bu[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, iki şeklin yapıştırılmış mı yoksa bağlantılı mı olduğunu belirlemek için IsGlued ve IsConnected özelliklerini sunar.
#### **Bağlı veya Yapıştırılmış Şekillerin Doğrulanması Programlama Örneği**
Aşağıdaki kod parçası, iki şeklin bağlantılı mı yoksa yapıştırılmış mı olduğunu doğrular.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Set two shape ids
long ShapeIdOne = 15;
long ShapeIdTwo = 16;

// Get Visio page by name
Page page = diagram.Pages.GetPage("Page-3");

// Get Visio shapes by ids
Shape ShapedOne = page.Shapes.GetShape(ShapeIdOne);
Shape ShapedTwo = page.Shapes.GetShape(ShapeIdTwo);

// Determine whether shapes are connected
bool connected = ShapedOne.IsConnected(ShapedTwo);
Console.WriteLine("Shapes are connected: " + connected);

// Determine whether shapes are glued
bool glued = ShapedOne.IsGlued(ShapedTwo);
Console.WriteLine("Shapes are Glued: " + glued);

{{< /highlight >}}

## **Visio Şeklinin bir Şekil Grubunda Olup Olmadığını Doğrulayın**
Aspose.Diagram for .NET API, geliştiricilerin Visio şeklinin bir grup şekil içinde olup olmadığını doğrulamasını sağlar.
### **Şekil Grubunda Şeklin Doğrulanması**
bu[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)class, Visio şeklinin bir grup şeklinde olup olmadığını belirlemek için IsInGroup özelliklerini sunar.
#### **Şekiller Grubu Programlama Örneğinde Şeklin Doğrulanması**
Aşağıdaki kod parçası, şeklin bir grup şeklinde olup olmadığını doğrular.


{{< highlight csharp >}}
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(13).Shapes.GetShape(2);
Console.WriteLine("Is it in a Group: " + shape.IsInGroup());
{{< /highlight >}}

