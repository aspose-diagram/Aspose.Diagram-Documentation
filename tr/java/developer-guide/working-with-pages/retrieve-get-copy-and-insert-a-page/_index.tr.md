---
title: Sayfa Al, Al, Kopyala ve Ekle
type: docs
weight: 10
url: /tr/java/retrieve-get-copy-and-insert-a-page/
---
## **Sayfa Bilgileri Alınıyor**
Microsoft Visio'de sayfalar ya ön plan ya da arka plan sayfalarıdır. Örneğin sayfa kimliği ve sayfa adı gibi sayfa bilgilerini almak için önce bir sayfanın arka plan mı yoksa ön plan sayfası mı olduğunu belirleyin.

 bu[Sayfa](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page)nesne, ön plan sayfasının veya arka plan sayfasının çizim alanını temsil eder. Tarafından sunulan Pages özelliği[Diagram](https://reference.aspose.com/diagram/java) class, Aspose.Diagram.Page nesnelerinin koleksiyonunu destekler. Bu özellik, sayfa bilgilerini almak için kullanılabilir.

Bir sayfanın ön plan mı yoksa arka plan sayfası mı olduğunu belirlemek için Page.Background özelliğini kullanın.

Aşağıdaki resim, bu makaledeki kod parçacıklarının çıktısını göstermektedir.

**Çıktıyı gösteren bir konsol.** 

![yapılacaklar:resim_alternatif_Metin](retrieve-get-copy-and-insert-a-page_1.png)
### **Sayfa Bilgilerini Al Programlama Örneği**
Aşağıdaki kod parçası, sayfa bilgilerini bir diagram'den alır.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrievePageInfo.class);

//Call the diagram constructor to load diagram
Diagram diagram = new Diagram(dataDir+ "RetrievePageInfo.vdx");

for (Page page : (Iterable<Page>) diagram.getPages())
{
    //Checks if current page is a background page
    if (page.getBackground() == com.aspose.diagram.BOOL.TRUE)
    {
        //Display information about the background page
        System.out.println("Background Page ID : " + page.getID());
        System.out.println("Background Page Name : " + page.getName());
    }
    else
    {
        //Display information about the foreground page
        System.out.println("\nPage ID : " + page.getID());
        System.out.println("Universal Name : " + page.getNameU());
        System.out.println("ID of the Background Page : " + page.getBackPage());
    }
}

{{< /highlight >}}
```
## **Bir Diagram'den Visio Sayfasını Alın**
Bazen, geliştiricilerin Visio numaralı çizimin sayfa ayrıntılarını alması gerekir. Aspose.Diagram, bunu yapmalarına yardımcı olan özelliklere sahiptir.

 Aspose.Diagram for Java sunuyor[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) Visio çizimini temsil eden sınıf. Diagram sınıfı tarafından sunulan Pages özelliği, Aspose.Diagram.Page nesnelerinin bir koleksiyonunu destekler. PageCollection sınıfı, Page nesnesini almak için çağrılabilen GetPage yöntemini gösterir.
### **Kimliğe göre Visio Sayfa Nesnesi Alma**
Bu örnek şu şekilde çalışır:

1. Diagram sınıfından bir nesne oluşturun.
1. Diagram.Pages sınıfının GetPage yöntemini çağırın.

Aşağıdaki örnek, Visio çiziminden kimliğe göre bir sayfa nesnesinin nasıl alınacağını gösterir.
#### **Kimliğe Göre Sayfa Nesnesi Al Programlama Örneği**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetVisioPagebyID.class); 
// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page id
int pageid = 2;
// Get page object by id
Page page2 = diagram.getPages().getPage(pageid);

{{< /highlight >}}
```
### **Ada Göre Visio Sayfa Nesnesi Alma**
Bu örnek şu şekilde çalışır:

1. Diagram sınıfından bir nesne oluşturun.
1. Diagram.Pages sınıfının GetPage yöntemini çağırın.
#### **Ada Göre Sayfa Nesnesi Al Programlama Örneği**
Aşağıdaki örnek, Visio çiziminden ada göre bir sayfa nesnesinin nasıl alınacağını gösterir.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetVisioPagebyName.class);     
// Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page name
String pageName = "Flow 2";
// Get page object by name
Page page2 = diagram.getPages().getPage(pageName);

{{< /highlight >}}
```
## **Bir Visio Sayfasını Başka Bir Diagram'e Kopyalayın**
Aspose.Diagram for Java API, geliştiricilerin içeriğini bir Visio diagram'den diğerine kopyalamasına ve eklemesine olanak tanır. Bu yardım konusu, bu görevin nasıl gerçekleştirileceğini açıklar.

 Aspose.Diagram for Java API'de var[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) Visio çizimini temsil eden sınıf. Diagram sınıfı tarafından sunulan Pages özelliği, Aspose.Diagram.Page nesnelerinin bir koleksiyonunu destekler. PageCollection sınıfı, başka bir Sayfa nesnesi eklemek için çağrılabilen Add yöntemini gösterir.

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

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CopyVisioPage.class);
        
// Call the diagram constructor to load diagram from a VSD file
Diagram originalDiagram = new Diagram(dataDir + "Drawing1.vsd");

// initialize the new visio diagram
Diagram newDiagram = new Diagram();

// add all masters from the source Visio diagram
MasterCollection originalMasters = originalDiagram.getMasters();
for (Master master : (Iterable<Master>) originalMasters) {
   newDiagram.addMaster(originalDiagram, master.getName());
}

// get the page object from the original diagram
Page SrcPage = originalDiagram.getPages().getPage("Page-1");
// set page name
SrcPage.setName("new page");
        
// it calculates max page id
int max = 0;
if (newDiagram.getPages().getCount() != 0)
    max = newDiagram.getPages().get(0).getID();

for (int i = 1; i < newDiagram.getPages().getCount(); i++)
{
    if (max < newDiagram.getPages().get(i).getID())
        max = newDiagram.getPages().get(i).getID();
}
       
int MaxPageId = max;
// set page id
SrcPage.setID(MaxPageId);
// add reference of the original diagram page
newDiagram.getPages().add(SrcPage);

// remove first empty page
newDiagram.getPages().remove(newDiagram.getPages().get(0));

// save diagram in VDX format
newDiagram.save(dataDir + "CopyVisioPage_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Visio Sayfasını başka bir Sayfa örneğine kopyalayın**
Page sınıfının Copy yöntemi, klonlamak için bir sayfa örneği alır.

**Java**

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page();

// copy page

newPage.copy(diagram.getPages().getPage("Page-1"));

{{< /highlight >}}
## **Visio Çizimine Boş Sayfa Ekleme**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) Microsoft Office Visio çizimine yeni bir boş sayfa ekleyebilir. Bu örnek konuda bunun nasıl yapılacağı açıklanmaktadır.

Sayfa koleksiyonu tarafından sunulan Add yöntemi, geliştiricilerin Visio diagram'de yeni bir boş sayfa eklemesine olanak tanır. Sayfa kimliği atanmalıdır.
### **Boş Sayfa Programlama Örneği Ekleme**
Aşağıdaki kod parçası, Visio Çizimine boş bir sayfa ekler:

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(InsertBlankPageInVisio.class);   
// load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
        
// it calculates max page id
int max = 0;
if (diagram.getPages().getCount() != 0)
    max = diagram.getPages().get(0).getID();

for (int i = 1; i < diagram.getPages().getCount(); i++)
{
    if (max < diagram.getPages().get(i).getID())
        max = diagram.getPages().get(i).getID();
}
        
// Initialize a new page object
Page newPage = new Page();
// Set name
newPage.setName("new page");
// Set page ID
newPage.setID(max + 1);

// Or try the Page constructor
// Page newPage = new Page(MaxPageId + 1);

// Add a new blank page
diagram.getPages().add(newPage);

// Save diagram
diagram.save(dataDir + "InsertBlankPageInVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Visio çiziminde Sayfa konumunu taşı**
Aspose.Diagram for Java API Visio çiziminde sayfa konumunu kaydırabilir. Page sınıfı tarafından sunulan moveTo yöntemi, geliştiricilerin sayfa konumunu taşımasına yardımcı olur.
### **Sayfa konumunu taşı Programlama Örneği**
MoveTo üyesi, Visio çiziminde sayfanın konumunu taşımak için hedef sayfa dizinini parametre olarak alır:

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.moveTo(2);

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
