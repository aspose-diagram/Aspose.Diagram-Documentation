---
title: Şekilleri Gruplandırın, Dönüştürün ve Doğrulayın
type: docs
weight: 50
url: /tr/java/group-convert-and-verify-shapes/
---
## **Visio Çiziminde Birden Fazla Şekli Birlikte Gruplandırın**
Aspose.Diagram API, geliştiricilerin şekilleri bir arada gruplandırmasına ve hepsini aynı anda taşımasına olanak tanır. Bir gruptaki her şekil benzersiz bir kimliğe sahiptir ve kendi özelliklerine sahiptir. Bir şekil grubunun biçimlendirmesini değiştirdiğimizde, her şekle yeni özellik atar.
### **Şekiller Nasıl Gruplandırılır?**
ShapeCollection sınıfı tarafından sunulan Group yöntemi, şekilleri birlikte gruplandırmak için kullanılabilir.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir numune yükleyin diagram.
1. şekillerin bir dizisini başlattı
1. kimliğe göre belirli bir şekil elde edin.
1. kimliğe göre başka bir özel şekil elde edin.
1. diziye şekiller atayın.
1. Group yöntemini çağırarak şekilleri gruplandırın.
1. kaydet diagram
#### **Grup Şekilleri Programlama Örneği**
Aspose.Diagram for Java API'i kullanarak şekilleri gruplandırmak için Java uygulamanızda aşağıdaki kodu kullanın.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GroupShapes.class);
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");

// Initialize an array of shapes
Shape[] ss = new Shape[3];

// extract and assign shapes to the array
ss[0] = page.getShapes().getShape(15);
ss[1] = page.getShapes().getShape(16);
ss[2] = page.getShapes().getShape(17);

// mark array shapes as group
page.getShapes().group(ss);

// save visio diagram
diagram.save(dataDir + "GroupShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Visio Şeklini Diğer Dosya Biçimlerine Dönüştürme**
Aspose.Diagram for Java API, geliştiricilerin tek bir Visio şeklini desteklenen diğer herhangi bir dosya biçimine dönüştürmesine olanak tanır. Bu yazıda, diğer tüm Visio şekillerini sayfadan kaldırıyoruz ve sayfa ayarını kaynak Şekil boyutuna göre özelleştiriyoruz.
### **Belirli Bir Şekli Dönüştürme Visio**
 Geliştiriciler, bir Visio şeklini şu şekilde PDF, HTML, Image, SVG ve SWF'e dönüştürebilir.[Visio kaydetme seçeneklerini belirleme]().
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
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SaveVisioShapeInOtherFormats.class);   
        
double shapeWidth = 0;
double shapeHeight = 0;

// call a Diagram class constructor to load the VSDX diagram
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");
// get Visio page
Page srcPage = srcVisio.getPages().get(1);
// remove background page
srcPage.setBackPage(null);

// get hash table of shapes, it holds id and name
Hashtable<Long, String> remShapes = new Hashtable<Long, String>();
for (Shape shape : (Iterable<Shape>)srcPage.getShapes())
    // for the normal shape
    remShapes.put(shape.getID(), shape.getName());
        

// iterate through the hash table
Enumeration<Long> enumKey = remShapes.keys();
while(enumKey.hasMoreElements())
{
    Long key = enumKey.nextElement();
    String val = remShapes.get(key);
    Shape shape = srcPage.getShapes().getShape(key);
    // check of the shape name
    if(val.equals("GroupShape1"))
    {
        // move shape to the origin corner
        shapeWidth = shape.getXForm().getWidth().getValue();
        shapeHeight = shape.getXForm().getHeight().getValue();
        shape.moveTo(shapeWidth*0.5, shapeHeight*0.5);
        // trim page size
        srcPage.getPageSheet().getPageProps().getPageWidth().setValue(shapeWidth);
        srcPage.getPageSheet().getPageProps().getPageHeight().setValue(shapeHeight);
    }
    else
    {
        // remove shape from the Visio page and hash table
        srcPage.getShapes().remove(shape);
        remShapes.remove(key);
    }
}

// specify saving options
PdfSaveOptions opts = new PdfSaveOptions();
// set page count to save
opts.setPageCount(1);
// set starting index of the page
opts.setPageIndex(1);
// save it
srcVisio.save(dataDir + "SaveVisioShapeInOtherFormats_Out.pdf", opts);

{{< /highlight >}}
```
### **Visio Şeklini PDF'e dönüştür**
Shape sınıfının ToPdf yöntemi, bir şekli PDF biçimine dönüştürmeye olanak tanır.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Visio Şeklini HTML'e dönüştür**
Shape sınıfının ToHTML yöntemi, bir şeklin HTML biçimine dönüştürülmesine izin verir.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

HTMLSaveOptions hs = new HTMLSaveOptions();

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}

{{% alert color="primary" %}} 

 Soru ve önerilerinizi şu adrese bekliyoruz:[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Derhal cevap vereceğiz.

{{% /alert %}} 
## **İki Visio Şeklin Bağlantılı veya Yapıştırılmış Olduğunu Doğrulayın**
 Aspose.Diagram for Java API, geliştiricilerin iki Visio şeklinin yapıştırıldığını veya bağlantılı olduğunu doğrulamasına olanak tanır. Daha önce, bu yardım konularında iki şekli nasıl birleştirebileceğimizi veya yapıştırabileceğimizi gördük:[Ekle ve Bağla Visio Şekiller](/diagram/tr/java/add-and-connect-visio-shapes/) ve[Kabın İçindeki Tutkal Şekilleri](/diagram/tr/java/working-with-shapes-gluing/).
### **Bağlı veya Yapıştırılmış Şekillerin Doğrulanması**
 bu[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class, iki şeklin yapıştırılmış mı yoksa bağlantılı mı olduğunu belirlemek için IsGlued ve IsConnected özelliklerini sunar.
#### **Bağlı veya Yapıştırılmış Şekillerin Doğrulanması Programlama Örneği**
Aşağıdaki kod parçası, iki şeklin bağlantılı mı yoksa yapıştırılmış mı olduğunu doğrular.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VerifyConnectedOrGluedShapes.class);  
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// set two shape ids
long ShapeIdOne = 15;
long ShapeIdTwo = 16;

// get Visio page by name
Page page = diagram.getPages().getPage("Page-3");

// get Visio shapes by ids
Shape ShapedOne = page.getShapes().getShape(ShapeIdOne);
Shape ShapedTwo = page.getShapes().getShape(ShapeIdTwo);

// determine whether shapes are connected
boolean connected = ShapedOne.isConnected(ShapedTwo);
System.out.println("Shapes are connected: " + connected);

// determine whether shapes are glued
boolean glued = ShapedOne.isGlued(ShapedTwo);
System.out.println("Shapes are Glued: " + glued);

{{< /highlight >}}
```
## **Visio Şeklinin bir Şekil Grubunda Olup Olmadığını Doğrulayın**
Aspose.Diagram for Java API, geliştiricilerin Visio şeklinin bir grup şekil içinde olup olmadığını doğrulamasını sağlar.
### **Şekil Grubunda Şeklin Doğrulanması**
Shape sınıfı, Visio şeklinin bir grup şeklinde olup olmadığını belirlemek için IsInGroup özellikleri sunar.
#### **Şekiller Grubu Programlama Örneğinde Şeklin Doğrulanması**
Aşağıdaki kod parçası, şeklin bir grup şeklinde olup olmadığını doğrular.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveTheParentShape.class) + "Shapes\\";
				
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(13).getShapes().getShape(2);
System.out.println("Is it in a Group: " + shape.isInGroup());
{{< /highlight >}}
```

{{% alert color="primary" %}} 

 Soru ve önerilerinizi şu adrese bekliyoruz:[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Derhal cevap vereceğiz.

{{% /alert %}}
