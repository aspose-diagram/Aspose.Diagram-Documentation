---
title: Görüntülerle Çalışmak
type: docs
weight: 60
url: /tr/net/working-with-images/
description: Bu bölüm, visio sayfasından Aspose.Diagram ile nasıl görüntü ekleneceğini veya görüntü alınacağını açıklar.
---
## **Visio Sayfasından Tüm Resimleri Çıkarın**
Microsoft Visio'de sayfalar ya ön plan ya da arka plan sayfalarıdır. Visio dosyasının belirli bir sayfasından görüntüleri çıkarabilirsiniz.
### **Görüntüleri Çıkar**
Sayfa Sınıfı nesnesi, bir ön plan sayfasının veya bir arka plan sayfasının çizim alanını temsil eder. Diagram sınıfı tarafından sunulan Shapes özelliği, Aspose.Diagram.Shape nesnelerinin bir koleksiyonunu destekler. Bu özellik, belirli bir sayfadaki tüm görüntüleri çıkarmak için kullanılabilir.
#### **Görüntüleri Çıkarma Programlama Örneği**
Aşağıdaki kod parçası, belirli bir Visio sayfasından tüm resimleri çıkarır.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");

// Enter page index i.e. 0 for first one
foreach (Shape shape in diagram.Pages[0].Shapes)
{
    // Filter shapes by type Foreign
    if (shape.Type == Aspose.Diagram.TypeValue.Foreign)
    {
        using (System.IO.MemoryStream stream = new System.IO.MemoryStream(shape.ForeignData.Value))
        {
            // Load memory stream into bitmap object
            System.Drawing.Bitmap bitmap = new System.Drawing.Bitmap(stream);

            // Save bmp here
            bitmap.Save(dataDir + "ExtractAllImages" + shape.ID + "_out.bmp");
        }
    }
}

{{< /highlight >}}
```
## **Çeşitli Visio Şekillerinin Simgelerini Alın**
Aspose.Diagram for .NET API artık geliştiricilerin çeşitli Visio şekillerine sahip simgeler almasına izin veriyor.
### **Şekil Simgesini Alma**
Aşağıdaki örneklerdeki kod, nasıl yapılacağını gösterir:

1. Mevcut bir diagram veya şablonu yükleyin.
1. Ana dizine göre alın
1. Ana simgeyi alın.
1. Simgeyi yerel alana kaydedin.
#### **Simge Programlama Örneği Alın**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load stencil file to a diagram object
Diagram stencil = new Diagram(dataDir + "Timeline.vss");
// Get master
Master master = stencil.Masters.GetMaster(1);

using (System.IO.MemoryStream stream = new System.IO.MemoryStream(master.Icon))
{
    // Load memory stream into bitmap object
    System.Drawing.Bitmap bitmap = new System.Drawing.Bitmap(stream);
    // Save as png format
    bitmap.Save(dataDir + "MasterIcon_out.png", System.Drawing.Imaging.ImageFormat.Png);
}

{{< /highlight >}}
```
## **Visio Diagram'in Resim Şeklini Değiştirme**
Aspose.Diagram for .NET API, geliştiricilerin Visio diagram'deki mevcut resim şekillerine erişmesine ve bunları değiştirmesine olanak tanır.
### **Resim Şeklini Değiştirme**
Aşağıdaki örneklerdeki kod, nasıl yapılacağını gösterir:

1. Mevcut bir diagram yükleyin.
1. Seçici sayfa şekillerini yineleyin.
1. Resim şekilleri elde etmek için filtre uygulayın.
1. Ortaya çıkan Visio diagram'i yerel alana kaydedin.
#### **Bir Resim Şekli Programlama Örneğinin Değiştirilmesi**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");
// Convert image into bytes array
byte[] imageBytes = File.ReadAllBytes(dataDir + "Picture.png");

// Enter page index i.e. 0 for first one
foreach (Shape shape in diagram.Pages[0].Shapes)
{
    // Filter shapes by type Foreign
    if (shape.Type == Aspose.Diagram.TypeValue.Foreign)
    {
        using (System.IO.MemoryStream stream = new System.IO.MemoryStream(shape.ForeignData.Value))
        {
            // Replace picture shape
            shape.ForeignData.Value = imageBytes;
        }
    }
}

// Save diagram
diagram.Save(dataDir + "ReplaceShapePicture_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Bitmap Görüntüsünü Visio Şekli Olarak İçe Aktar**
Aspose.Diagram for .NET API artık geliştiricilerin bir bitmap görüntüsünü Microsoft Visio şekli olarak içe aktarmasına izin veriyor.
### **Visio'e bir BMP Görüntüsü ekleyin**
Aşağıdaki örneklerdeki kod, nasıl yapılacağını gösterir:

1. Bir diagram oluşturun.
1. Visio sayfasını edinin
1. Bir bitmap görüntüsünü Visio şekli olarak içe aktarın
1. diagram'i kaydedin.
#### **BMP Görüntü Programlama Örneği ekleyin**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Create a new diagram
Diagram diagram = new Diagram();

// Get page object by index
Page page0 = diagram.Pages[0];
// Set pinX, pinY, width and height
double pinX = 2, pinY = 2, width = 4, hieght = 3;

// Import Bitmap image as Visio shape
page0.AddShape(pinX, pinY, width, hieght, new FileStream(dataDir + "image.bmp", FileMode.OpenOrCreate));

// Save Visio diagram
diagram.Save(dataDir + "InsertImageInVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Visio Sayfanın Belirtilen Alanını Görüntüye Dönüştür**
Aspose.Diagram for .NET API ile geliştiriciler, XY koordinatları, genişlik ve yükseklik ile bir alan tanımlayabilir ve ardından bu alanı desteklenen bir görüntü formatına dönüştürebilir.
### **Visio çizim alanını bir Resme dönüştürün**
Aşağıdaki örneklerdeki kod, nasıl yapılacağını gösterir:

1. Mevcut bir Visio çizimini yükleyin
1. Dikdörtgen alanı tanımla
1. Belirtilen alanı bir görüntüye dönüştürün

**C#**

{{< highlight "java" >}}

 // load a Visio drawing

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

Aspose.Diagram.Saving.ImageSaveOptions Options = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);

// specify region with XY coordinates, width and height

Options.Area = new RectangleF(0, 0, 1, 1);

// save into the image format

diagram.Save(@"c:\temp\area.png", Options);

{{< /highlight >}}
