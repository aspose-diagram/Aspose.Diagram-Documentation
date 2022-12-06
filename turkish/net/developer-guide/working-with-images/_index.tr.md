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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-ExtractAllImagesFromPage-ExtractAllImagesFromPage.cs" >}}
## **Çeşitli Visio Şekillerinin Simgelerini Alın**
Aspose.Diagram for .NET API artık geliştiricilerin çeşitli Visio şekillerine sahip simgeler almasına izin veriyor.
### **Şekil Simgesini Alma**
Aşağıdaki örneklerdeki kod, nasıl yapılacağını gösterir:

1. Mevcut bir diagram veya şablonu yükleyin.
1. Ana dizine göre alın
1. Ana simgeyi alın.
1. Simgeyi yerel alana kaydedin.
#### **Simge Programlama Örneği Alın**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-GetShapeIcon-GetShapeIcon.cs" >}}
## **Visio Diagram'in Resim Şeklini Değiştirme**
Aspose.Diagram for .NET API, geliştiricilerin Visio diagram'deki mevcut resim şekillerine erişmesine ve bunları değiştirmesine olanak tanır.
### **Resim Şeklini Değiştirme**
Aşağıdaki örneklerdeki kod, nasıl yapılacağını gösterir:

1. Mevcut bir diagram yükleyin.
1. Seçici sayfa şekillerini yineleyin.
1. Resim şekilleri elde etmek için filtre uygulayın.
1. Ortaya çıkan Visio diagram'i yerel alana kaydedin.
#### **Bir Resim Şekli Programlama Örneğinin Değiştirilmesi**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-ReplaceShapePicture-ReplaceShapePicture.cs" >}}
## **Bitmap Görüntüsünü Visio Şekli Olarak İçe Aktar**
Aspose.Diagram for .NET API artık geliştiricilerin bir bitmap görüntüsünü Microsoft Visio şekli olarak içe aktarmasına izin veriyor.
### **Visio'de bir BMP Görüntüsü ekleyin**
Aşağıdaki örneklerdeki kod, nasıl yapılacağını gösterir:

1. Bir diagram oluşturun.
1. Visio sayfasını edinin
1. Bir bitmap görüntüsünü Visio şekli olarak içe aktarın
1. diagram'i kaydedin.
#### **Bir BMP Görüntü Programlama Örneği Ekleme**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-InsertImageInVisio-InsertImageInVisio.cs" >}}
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
