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

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-RetrievePageInfo-RetrievePageInfo.java" >}}
## **Bir Diagram'den Visio Sayfasını Alın**
Bazen, geliştiricilerin Visio numaralı çizimin sayfa ayrıntılarını alması gerekir. Aspose.Diagram, bunu yapmalarına yardımcı olan özelliklere sahiptir.

 Aspose.Diagram for Java sunuyor[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) Visio çizimini temsil eden sınıf. Diagram sınıfı tarafından sunulan Pages özelliği, Aspose.Diagram.Page nesnelerinin bir koleksiyonunu destekler. PageCollection sınıfı, Page nesnesini almak için çağrılabilen GetPage yöntemini gösterir.
### **Kimliğe göre Visio Sayfa Nesnesi Alma**
Bu örnek şu şekilde çalışır:

1. Diagram sınıfından bir nesne oluşturun.
1. Diagram.Pages sınıfının GetPage yöntemini çağırın.

Aşağıdaki örnek, Visio çiziminden kimliğe göre bir sayfa nesnesinin nasıl alınacağını gösterir.
#### **Kimliğe Göre Sayfa Nesnesi Al Programlama Örneği**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-GetVisioPagebyID-GetVisioPagebyID.java" >}}
### **Ada Göre Visio Sayfa Nesnesi Alma**
Bu örnek şu şekilde çalışır:

1. Diagram sınıfından bir nesne oluşturun.
1. Diagram.Pages sınıfının GetPage yöntemini çağırın.
#### **Ada Göre Sayfa Nesnesi Al Programlama Örneği**
Aşağıdaki örnek, Visio çiziminden ada göre bir sayfa nesnesinin nasıl alınacağını gösterir.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-GetVisioPagebyName-GetVisioPagebyName.java" >}}
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

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-CopyVisioPage-CopyVisioPage.java" >}}
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

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-InsertBlankPageInVisio-InsertBlankPageInVisio.java" >}}
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
