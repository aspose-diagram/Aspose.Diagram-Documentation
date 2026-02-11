---
title: Görüntülerle Çalışmak
type: docs
weight: 70
url: /tr/java/working-with-images/
---
## **Visio Sayfasından Tüm Resimleri Çıkarın**
Microsoft Visio'de sayfalar ya ön plan ya da arka plan sayfalarıdır. Visio dosyasının belirli bir sayfasından görüntüleri çıkarabilirsiniz.
### **Görüntüleri Çıkar**
Sayfa Sınıfı nesnesi, bir ön plan sayfasının veya bir arka plan sayfasının çizim alanını temsil eder. Diagram sınıfı tarafından sunulan Shapes özelliği, Aspose.Diagram.Shape nesnelerinin bir koleksiyonunu destekler. Bu özellik, belirli bir sayfadaki tüm görüntüleri çıkarmak için kullanılabilir.
#### **Görüntüleri Çıkarma Programlama Örneği**
Aşağıdaki kod parçası, belirli bir Visio sayfasından tüm resimleri çıkarır.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExtractAllImagesFromPage.class);
// call a Diagram class constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");

// Enter page index i.e. 0 for first one
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage(0).getShapes())
{
    // Filter shapes by type Foreign
    if (shape.getType() == TypeValue.FOREIGN)
    {
        FileOutputStream fos = new FileOutputStream(dataDir+ "ExtractAllImages" + shape.getID() + "_Out.bmp");
        fos.write(shape.getForeignData().getValue());
        fos.close();
    }
}

{{< /highlight >}}
```
## **Çeşitli Visio Şekillerinin Simgelerini Alın**
Aspose.Diagram for Java API artık geliştiricilerin çeşitli Visio şekillerine sahip simgeler almasına izin veriyor.
### **Şekil Simgesini Alma**
Aşağıdaki örneklerdeki kod, nasıl yapılacağını gösterir:

1. Mevcut bir diagram veya şablonu yükleyin.
1. Ana dizine göre alın
1. Ana simgeyi alın.
1. Simgeyi yerel alana kaydedin.
#### **Simge Programlama Örneği Alın**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetShapeIcon.class);  
// Load stencil file to a diagram object
Diagram stencil = new Diagram(dataDir + "Timeline.vss");
// get master
Master master = stencil.getMasters().getMasterByName("Triangle");
// get byte array
byte[] bytes = master.getIcon();
// create an image file
FileOutputStream fos = new FileOutputStream(dataDir + "MasterIcon_Out.png");
// write byte array of the image
fos.write(bytes);
// close array
fos.close();

{{< /highlight >}}
```
## **Visio Diagram'in Resim Şeklini Değiştirme**
Aspose.Diagram for Java API, geliştiricilerin Visio diagram'deki mevcut resim şekillerine erişmesine ve bunları değiştirmesine olanak tanır.
### **Resim Şeklini Değiştirme**
Aşağıdaki örneklerdeki kod, nasıl yapılacağını gösterir:

1. Mevcut bir diagram yükleyin.
1. Seçici sayfa şekillerini yineleyin.
1. Resim şekilleri elde etmek için filtre uygulayın.
1. Ortaya çıkan Visio diagram'i yerel alana kaydedin.
#### **Bir Resim Şekli Programlama Örneğinin Değiştirilmesi**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReplaceShapePicture.class); 
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");
        
// convert image into bytes array       
File fi = new File(dataDir + "Picture.png");
byte[] fileContent = Files.readAllBytes(fi.toPath());
		
// Enter page index i.e. 0 for first one
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage(0).getShapes())
{
    // Filter shapes by type Foreign
    if (shape.getType() == TypeValue.FOREIGN)
    {
        //replace picture shape
    	shape.getForeignData().setValue(fileContent);
    }
}

// save diagram
diagram.save(dataDir + "ReplaceShapePicture_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Bitmap Görüntüsünü Visio Şekli Olarak İçe Aktar**
Aspose.Diagram for Java API artık geliştiricilerin bir bitmap görüntüsünü Microsoft Visio şekli olarak içe aktarmasına izin veriyor.
### **Visio'e bir BMP Görüntüsü ekleyin**
Aşağıdaki örneklerdeki kod, nasıl yapılacağını gösterir:

1. Bir diagram oluşturun.
1. Visio sayfasını edinin
1. Bir bitmap görüntüsünü Visio şekli olarak içe aktarın
1. diagram'i kaydedin.
#### **BMP Görüntü Programlama Örneği ekleyin**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExtractAllImagesFromPage.class);
// call a Diagram class constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");

// Enter page index i.e. 0 for first one
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage(0).getShapes())
{
    // Filter shapes by type Foreign
    if (shape.getType() == TypeValue.FOREIGN)
    {
        FileOutputStream fos = new FileOutputStream(dataDir+ "ExtractAllImages" + shape.getID() + "_Out.bmp");
        fos.write(shape.getForeignData().getValue());
        fos.close();
    }
}

{{< /highlight >}}
```
