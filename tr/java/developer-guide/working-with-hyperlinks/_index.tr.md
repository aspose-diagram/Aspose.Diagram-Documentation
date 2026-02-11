---
title: Köprülerle Çalışmak
type: docs
weight: 110
url: /tr/java/working-with-hyperlinks/
---
## **Visio Şekline Köprü Ekleme**
Microsoft Visio şekline dinamik olarak köprü eklemek kolay bir yaklaşımdır.

Çok sayfalı Visio çizimlerinde köprüler sizi bir sayfadan diğerine taşıyabilir. Ayrıca çiziminizi bir web sayfasına veya sisteminizdeki bir dosyaya bağlayabilirsiniz.

Bu özellikler,[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) sınıfı destekler[com.aspose.diagram.Hyperlink](https://reference.aspose.com/diagram/java/com.aspose.diagram/hyperlink) nesne. Add yöntemi, bir şeklin köprü verilerini eklemek için kullanılabilir.

Microsoft Visio'deki özellikleri tanımlamak için:

1. diagram'de bir şekle sağ tıklayın.
1.  Seçme**köprü**.
1. Mevcut özellikleri ayarla
1.  Basmak**TAMAM** buton

**Microsoft Visio'de görüldüğü gibi bir şeklin köprü verileri**

![yapılacaklar:resim_alternatif_Metin](working-with-hyperlinks_1.png)

Aşağıdaki kod parçacıkları, şeklin köprü verilerini ekler.
### **Köprü Programlama Örneği Ekle**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddHyperlinkToShape.class);   
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by ID
Shape shape = page.getShapes().getShape(2);

//initialize Hyperlink object
Hyperlink hyperlink = new Hyperlink();
//set address value
hyperlink.getAddress().setValue("http://www.google.com/");
//set sub address value
hyperlink.getSubAddress().setValue("Sub address here");
//set description value
hyperlink.getDescription().setValue("Description here");
//set name
hyperlink.setName("MyHyperLink");

//add hyperlink to the shape
shape.getHyperlinks().add(hyperlink);            
//save diagram to local space
diagram.save(dataDir + "AddHyperlinkToShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Visio Şekillerinin Köprü Verilerini Alın**
 Bir şeklin köprü verilerini, sizin yaptığınıza benzer bir şekilde elde etmek mümkündür.[Visio şekil verisi okunuyor]().

Geliştiriciler, bir Visio şeklinden tüm köprüleri aldıkları gibi alabilirler.[Visio şekil verisini oku]() kullanarak[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/)

Çok sayfalı Visio çizimlerde, köprüler sizi bir sayfadan diğerine taşıyabilir. Ayrıca çiziminizi bir web sayfasına veya sisteminizdeki bir dosyaya bağlayabilirsiniz.

Bu özellikler,[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) sınıfı destekler[com.aspose.diagram.Hyperlink](https://reference.aspose.com/diagram/java/com.aspose.diagram/hyperlink)nesne. Özellik, bir şeklin köprü verilerini okumak için kullanılabilir.

Microsoft Visio'deki özellikleri tanımlamak için:

1. diagram'de bir şekle sağ tıklayın.
1.  Seçme**köprü.**
 Varolan tüm özellikler iletişim kutusunda listelenir.

**Microsoft Visio'de görüldüğü gibi bir şeklin köprü verileri**

![yapılacaklar:resim_alternatif_Metin](working-with-hyperlinks_2.png)

**Şekil verisi çıktısını gösteren bir konsol penceresi**

![yapılacaklar:resim_alternatif_Metin](working-with-hyperlinks_3.png)

Aşağıdaki kod parçacıkları, şeklin köprü verilerini okur.
### **Köprü Programlama Örneği Alın**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetHyperlinks.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by ID
Shape shape = page.getShapes().getShape(1);
// iterate through the hyperlinks
for (Hyperlink hyperlink :(Iterable<Hyperlink>) shape.getHyperlinks())
{
    System.out.println("Address: " + hyperlink.getAddress().getValue());
    System.out.println("Sub Address: " + hyperlink.getSubAddress().getValue());
    System.out.println("Description: " + hyperlink.getDescription().getValue());
}

{{< /highlight >}}

