---
title: Visio Bağlayıcıları ve Yazı Tipi Bilgilerini Alın
type: docs
weight: 20
url: /tr/net/retrieve-visio-connectors-and-font-information/
description: Bu bölümde visio konektörlerinin ve yazı tipi bilgilerinin nasıl alınacağı açıklanmaktadır.
---
## **Bağlayıcı Bilgilerini Alma**
 Aspose.Diagram for .NET, kimlik ve isim - hakkında bilgi almak için mekanizmalar sağlar[sayfalar](/diagram/tr/net/retrieve-2c-get-2c-copy-and-insert-a-page/) ve[usta](https://docs.aspose.com/diagram/net/working-with-masters/). Ayrıca, şekilleri birbirine bağlayan öğeler olan bağlayıcılar hakkında bilgi almanızı sağlar.

 bu[Bağlamak](http://www.aspose.com/api/net/diagram/aspose.diagram/connect) nesne, bir Visio çizim sayfasında iki şekli birleştiren bir bağlayıcıyı temsil eder. Tarafından sunulan Connects özelliği[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class, Aspose.Diagram.Connect nesnelerinin bir koleksiyonunu destekler. Bu özellik, bir bağlayıcı hakkında kimlik ve ad bilgilerini almak için kullanılabilir.
### **Programlama Örneği**
Aşağıdaki kod parçası, bir diagram'deki konektörler için bilgileri alır.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load diagram from a VSD file
Diagram vdxDiagram = new Diagram(dataDir + "RetrieveConnectorInfo.vsd");

foreach (Aspose.Diagram.Connect connector in vdxDiagram.Pages[0].Connects)
{
    // Display information about the Connectors
    Console.WriteLine("\nFrom Shape ID : " + connector.FromSheet);
    Console.WriteLine("To Shape ID : " + connector.ToSheet);
}

{{< /highlight >}}

## **Yazı Tipi Bilgilerini Alma**
 Aspose.Diagram, diagram'i oluşturan öğeler hakkında bilgi almak için mekanizmalara sahiptir.[sayfalar](/diagram/tr/net/retrieve-2c-get-2c-copy-and-insert-a-page/), [şablonlar](https://docs.aspose.com/diagram/net/working-with-masters/), [konektörler](/diagram/tr/net/retrieving-connector-information/)ve ayrıca yazı tipleri. Bu makale, bir diagram'de hangi yazı tiplerinin kullanıldığını nasıl bulacağınızı gösterir.

 bu[Yazı tipi](http://www.aspose.com/api/net/diagram/aspose.diagram/font) nesne, bir belgedeki metne uygulanan veya sistemde kullanılabilen bir yazı tipini temsil eder. Bir Yazı Tipi nesnesi, bir adı (örneğin, "Arial"), Microsoft Visio'in bu yazı tipiyle biçimlendirilmiş metni içeren bir şeklin Karakter bölümündeki Yazı Tipi hücresinde depoladığı yazı tipi kimliğine (örneğin, 3) eşler. Yazı tipi kimlikleri, bir belge farklı sistemlerde açıldığında veya yazı tipleri yüklendiğinde veya kaldırıldığında değişebilir.
### **Yazı Tipi Programlama Örneği Alınıyor**
Aşağıdaki kod parçası, Visio diagram'den yazı tipi bilgilerini alır.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load diagram from a VSD file
Diagram vdxDiagram = new Diagram(dataDir + "RetrieveFontInfo.vsd");

foreach (Aspose.Diagram.Font font in vdxDiagram.Fonts)
{
    // Display information about the fonts
    Console.WriteLine(font.Name);
}

{{< /highlight >}}

### **Varsayılan Yazı Tipi Dizinini Alma**
Aspose.Diagram for .NET API, Diagram Sınıfının GetDefaultFontDir() yöntemini kullanarak varsayılan yazı tipi dizini yolunun alınmasına da izin verir. Aşağıdaki kod parçası, Visio diagram'den varsayılan yazı tipi dizinini alır.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load diagram from a VSD file
Diagram vdxDiagram = new Diagram(dataDir + "RetrieveFontInfo.vsd");
           
// Display font default directory
Console.WriteLine(vdxDiagram.GetDefaultFontDir());

{{< /highlight >}}

### **Kullanılmayan Yazı Tiplerini Alma**
{{% alert color="primary" %}}

Bu yöntem, sürüm 19.6 veya üstü tarafından desteklenir.

{{% /alert %}}

Aspose.Diagram for .NET API ayrıca Diagram Sınıfı GetUnusedStyles() yöntemini kullanarak kullanılmayan yazı tiplerini almaya da izin verir. Aşağıdaki kod parçası, kullanılmayan yazı tiplerini Visio diagram'den alır.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load diagram from a VSD file
Diagram vdxDiagram = new Diagram(dataDir + "Sample_UnusedFonts.vsdx");

// Get Unused Fonts 
StyleSheetCollection unused = vdxDiagram.GetUnusedStyles();

// Display unused fonts count 
Console.WriteLine(unused.Count);

{{< /highlight >}}

