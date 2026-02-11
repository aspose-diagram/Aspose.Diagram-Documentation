---
title: Sayfa Al, Al, Kopyala ve Ekle
type: docs
weight: 10
url: /tr/net/retrieve-get-copy-and-insert-a-page/
description: Bu bölümde Aspose.Diagram ile sayfa ekleme, sayfa kopyalama veya sayfa bilgilerinin nasıl alınacağı açıklanmaktadır.
---
## **Sayfa Bilgileri Alınıyor**
Microsoft Visio'de sayfalar ya ön plan ya da arka plan sayfalarıdır. Örneğin sayfa kimliği ve sayfa adı gibi sayfa bilgilerini almak için önce bir sayfanın arka plan mı yoksa ön plan sayfası mı olduğunu belirleyin.

 bu[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page)nesne, ön plan sayfasının veya arka plan sayfasının çizim alanını temsil eder. Tarafından sunulan Pages özelliği[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class, Aspose.Diagram.Page nesnelerinin koleksiyonunu destekler. Bu özellik, sayfa bilgilerini almak için kullanılabilir.

Bir sayfanın ön plan mı yoksa arka plan sayfası mı olduğunu belirlemek için Page.Background özelliğini kullanın.
### **Sayfa Bilgilerini Al Programlama Örneği**
Aşağıdaki kod parçası, sayfa bilgilerini bir diagram'den alır.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Call the diagram constructor to load diagram from a VDX file
Diagram vdxDiagram = new Diagram(dataDir + "RetrievePageInfo.vdx");

foreach (Aspose.Diagram.Page page in vdxDiagram.Pages)
{
    // Checks if current page is a background page
    if (page.Background == Aspose.Diagram.BOOL.True)
    {
        // Display information about the background page
        Console.WriteLine("Background Page ID : " + page.ID);
        Console.WriteLine("Background Page Name : " + page.Name);
    }
    else
    {
        // Display information about the foreground page
        Console.WriteLine("\nPage ID : " + page.ID);
        Console.WriteLine("Universal Name : " + page.NameU);
        Console.WriteLine("ID of the Background Page : " + page.BackPage);
    }
}

{{< /highlight >}}

## **Bir Diagram'den Visio Sayfasını Alın**
Bazen, geliştiricilerin Visio numaralı çizimin sayfa ayrıntılarını alması gerekir. Aspose.Diagram, bunu yapmalarına yardımcı olan özelliklere sahiptir.

 Aspose.Diagram for .NET sunuyor[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Visio çizimini temsil eden sınıf. Diagram sınıfı tarafından sunulan Pages özelliği, Aspose.Diagram.Page nesnelerinin bir koleksiyonunu destekler. PageCollection sınıfı, Page nesnesini almak için çağrılabilen GetPage yöntemini gösterir.
### **Kimliğe göre Visio Sayfa Nesnesi Alma**
Bu örnek şu şekilde çalışır:

1. Diagram sınıfından bir nesne oluşturun.
1. Diagram.Pages sınıfının GetPage yöntemini çağırın.

Aşağıdaki örnek, Visio çiziminden kimliğe göre bir sayfa nesnesinin nasıl alınacağını gösterir.
#### **Kimliğe Göre Sayfa Nesnesi Al Programlama Örneği**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page id
int pageid = 2;
// Get page object by id
Page page2 = diagram.Pages.GetPage(pageid);

{{< /highlight >}}

### **Ada Göre Visio Sayfa Nesnesi Alma**
Bu örnek şu şekilde çalışır:

1. Diagram sınıfından bir nesne oluşturun.
1. Diagram.Pages sınıfının GetPage yöntemini çağırın.
#### **Ada Göre Sayfa Nesnesi Al Programlama Örneği**
Aşağıdaki örnek, Visio çiziminden ada göre bir sayfa nesnesinin nasıl alınacağını gösterir.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page name
string pageName = "Flow 2";
// Get page object by name
Page page2 = diagram.Pages.GetPage(pageName);

{{< /highlight >}}

## **Bir Visio Sayfasını Başka Bir Diagram'e Kopyalayın**
Aspose.Diagram for .NET API, geliştiricilerin içeriğini bir Visio diagram'den diğerine kopyalamasına ve eklemesine olanak tanır. Bu yardım konusu, bu görevin nasıl gerçekleştirileceğini açıklar.

 Aspose.Diagram for .NET API'de var[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Visio çizimini temsil eden sınıf. Diagram sınıfı tarafından sunulan Pages özelliği, Aspose.Diagram.Page nesnelerinin bir koleksiyonunu destekler. PageCollection sınıfı, başka bir Sayfa nesnesi eklemek için çağrılabilen Add yöntemini gösterir.

Bu örnek şu şekilde çalışır:

1. Diagram sınıfından yeni bir nesne oluşturun.
1. Mevcut bir Visio diagram'i Diagram sınıf nesnesine yükleyin.
1. Yüklenen Visio diagram'den tüm master'ları ekle
1. Yüklenen diagram'den (kopyalanması gereken) sayfa nesnesini alın.
1. Sayfa nesnesi adını ve kimliğini ayarlayın.
1. Yeni diagram'in boş sayfasını kaldırın (isteğe bağlı).
1. PageCollection sınıfının Add yöntemini çağırın.
1. Yeni diagram'i bilgisayar belleğine kaydedin.
### **Visio Sayfa Programlama Örneği Kopyalama**
Aşağıdaki kod örneği, bir Visio sayfa nesnesinin başka bir Visio çizimine nasıl kopyalanacağını gösterir.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram NewDigram = new Diagram();

// Load source diagram
Diagram dgm = new Diagram(dataDir + "Drawing1.vsdx");
// Add all masters from the source Visio diagram
foreach (Master master in dgm.Masters)
    NewDigram.Masters.Add(master);

// Get page object
Aspose.Diagram.Page SrcPage = dgm.Pages.GetPage("Page-1");
// Set name
SrcPage.Name = "new page";

// It calculates max page id
int max = 0;
if (NewDigram.Pages.Count != 0)
    max = NewDigram.Pages[0].ID;

for (int i = 1; i < NewDigram.Pages.Count; i++)
{
    if (max < NewDigram.Pages[i].ID)
        max = NewDigram.Pages[i].ID;
}
            
// Set max page ID 
int MaxPageId = max;
// Set page ID
SrcPage.ID = MaxPageId + 1;

// Add page from the source diagram
NewDigram.Pages.Add(SrcPage);
// Remove first empty page
NewDigram.Pages.Remove(NewDigram.Pages[0]);
// Save diagram
NewDigram.Save(dataDir + "CopyVisioPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Visio Sayfasını başka bir Sayfa örneğine kopyalayın**
Page sınıfının Copy yöntemi, klonlamak için bir sayfa örneği alır.

**C#**

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page();

// copy page

newPage.Copy(diagram.Pages.GetPage("Page-1"));

{{< /highlight >}}
## **Visio Çizimine Boş Sayfa Ekleme**
[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) Microsoft Office Visio çizimine yeni bir boş sayfa ekleyebilir. Bu örnek konuda bunun nasıl yapılacağı açıklanmaktadır.

Sayfa koleksiyonu tarafından sunulan Add yöntemi, geliştiricilerin Visio diagram'de yeni bir boş sayfa eklemesine olanak tanır. Sayfa kimliği atanmalıdır.
### **Boş Sayfa Programlama Örneği Ekleme**
Aşağıdaki kod parçası, Visio Çizimine boş bir sayfa ekler:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// It calculates max page id
int max = 0;
if (diagram.Pages.Count != 0)
    max = diagram.Pages[0].ID;

for (int i = 1; i < diagram.Pages.Count; i++)
{
    if (max < diagram.Pages[i].ID)
        max = diagram.Pages[i].ID;
}

// Set max page ID
int MaxPageId = max;

// Initialize a new page object
Page newPage = new Page();
// Set name
newPage.Name = "new page";
// Set page ID
newPage.ID = MaxPageId + 1;

// Or try the Page constructor
// Page newPage = new Page(MaxPageId + 1);

// Add a new blank page
diagram.Pages.Add(newPage);

// Save diagram
diagram.Save(dataDir + "InsertBlankPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Visio çiziminde Sayfa konumunu taşı**
Aspose.Diagram for .NET API Visio çiziminde sayfa konumunu kaydırabilir. Page sınıfı tarafından sunulan MoveTo yöntemi, geliştiricilerin sayfa konumunu taşımasına yardımcı olur.
### **Sayfa konumunu taşı Programlama Örneği**
MoveTo üyesi, Visio çiziminde sayfanın konumunu taşımak için hedef sayfa dizinini parametre olarak alır:

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.MoveTo(2);

diagram.Save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
