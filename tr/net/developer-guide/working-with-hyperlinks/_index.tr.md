---
title: Köprülerle Çalışmak
type: docs
weight: 160
url: /tr/net/working-with-hyperlinks/
description: Bu bölümde, Aspose.Diagram ile Visio Şeklinde Köprü ekleme veya Köprü alma açıklanmaktadır.
---
## **Visio Şekline Köprü Ekleme**
Microsoft Office Visio, köprülerin herhangi bir şekle eklenmesini destekler. Köprüler, geçerli çizimdeki başka bir sayfaya veya şekle, başka bir çizimdeki sayfaya veya şekle, Visio çizimi dışında bir belgeye, bir Web sitesine, FTP sitesine veya e-posta adresine bağlanabilir. Geliştiriciler, Visio şekline köprüleri kolayca eklemek için Aspose.Diagram API'i kullanabilir.

 Çok sayfalı Visio çiziminde, köprüler sizi bir şekilden diğer birçok bağlantı türüne yönlendirebilir.[Köprü Koleksiyonu](http://www.aspose.com/api/net/diagram/aspose.diagram/hyperlinkcollection) tarafından maruz[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, bir şeklin köprüsünü eklemek için kullanılabilecek Add yöntemini sunar.

Microsoft Office Visio'deki özellikleri tanımlamak için:

1. Visio diagram'de bir şekle sağ tıklayın.
1.  Seçme**köprü.**
1. Mevcut özellikleri ayarla
1.  Basmak**TAMAM** buton

**Microsoft Visio'de görüldüğü gibi bir şeklin köprü verileri**

![yapılacaklar:resim_alternatif_Metin](working-with-hyperlinks_1.png)
### **Köprü Programlama Örneği Ekle**
Aşağıdaki kod parçacığı, şeklin köprü verilerini ekler.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Hyperlinks();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(2);

// Initialize Hyperlink object
Hyperlink hyperlink = new Hyperlink();
// Set address value
hyperlink.Address.Value = "http:// Www.google.com/";
// Set sub address value
hyperlink.SubAddress.Value = "Sub address here";
// Set description value
hyperlink.Description.Value = "Description here";
// Set name
hyperlink.Name = "MyHyperLink";

// Add hyperlink to the shape
shape.Hyperlinks.Add(hyperlink);            
// Save diagram to local space
diagram.Save(dataDir + "AddHyperlinkToShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Visio Şekillerinin Köprü Verilerini Alın**
Geliştiriciler, bir Visio şeklinden tüm köprüleri aldıkları gibi alabilirler.[Visio şekil verisini oku](https://docs.aspose.com/diagram/net/load-or-create-a-visio-drawing/) kullanarak[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

Çok sayfalı Visio çiziminde, köprüler sizi bir şekilden diğer birçok bağlantı türüne yönlendirebilir.[Köprü Koleksiyonu](http://www.aspose.com/api/net/diagram/aspose.diagram/hyperlinkcollection) tarafından maruz[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, geliştiricilerin köprüleri almasına izin verir.

Microsoft Office Visio'deki özellikleri tanımlamak için:

1. diagram'de bir şekle sağ tıklayın.
1.  Seçme**köprü.**

Varolan tüm özellikler iletişim kutusunda listelenir.
**Microsoft Visio'de görüldüğü gibi bir şeklin köprü verileri**

![yapılacaklar:resim_alternatif_Metin](working-with-hyperlinks_1.png)

**Şekil verisi çıktısını gösteren bir konsol penceresi**

![yapılacaklar:resim_alternatif_Metin](working-with-hyperlinks_3.png)
### **Köprü Programlama Örneği Alın**
Aşağıdaki kod parçacığı, şeklin köprü verilerini okur.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Hyperlinks();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(1);
// Iterate through the hyperlinks
foreach (Aspose.Diagram.Hyperlink hyperlink in shape.Hyperlinks)
{
    Console.WriteLine("Address: " + hyperlink.Address.Value);
    Console.WriteLine("Sub Address: " + hyperlink.SubAddress.Value);
    Console.WriteLine("Description: " + hyperlink.Description.Value);
}       

{{< /highlight >}}
```
