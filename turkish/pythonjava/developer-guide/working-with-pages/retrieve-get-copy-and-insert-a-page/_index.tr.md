---
title: Sayfa Al, Al, Kopyala ve Ekle
type: docs
weight: 10
url: /tr/python-java/retrieve-get-copy-and-insert-a-page/
---
## **Sayfa Bilgileri Alınıyor**
Microsoft Visio'de sayfalar ya ön plan ya da arka plan sayfalarıdır. Örneğin sayfa kimliği ve sayfa adı gibi sayfa bilgilerini almak için önce bir sayfanın arka plan mı yoksa ön plan sayfası mı olduğunu belirleyin.

`Page` nesnesi, bir ön plan sayfasının veya bir arka plan sayfasının çizim alanını temsil eder. `Diagram` sınıfı tarafından sunulan Pages özelliği, bir Sayfa nesneleri koleksiyonunu destekler. Bu özellik, sayfa bilgilerini almak için kullanılabilir.

Bir sayfanın ön plan mı yoksa arka plan sayfası mı olduğunu belirlemek için `Page.Background` özelliğini kullanın.

### **Sayfa Bilgilerini Al Programlama Örneği**
Aşağıdaki kod parçası, sayfa bilgilerini bir diagram'den alır.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-RetrievePageInfo.py" >}}

## **Bir Diagram'den Visio Sayfasını Alın**
Bazen, geliştiricilerin Visio numaralı çizimin sayfa ayrıntılarını alması gerekir. Python için Aspose.Diagram via Java bunu yapmalarına yardımcı olan özelliklere sahiptir.

Python için Aspose.Diagram via Java, bir Visio çizimini temsil eden `Diagram` sınıfını sunar. Diagram sınıfı tarafından sunulan Pages özelliği, `Page` nesne koleksiyonunu destekler. PageCollection sınıfı, Page nesnesini almak için çağrılabilen `getPage` yöntemini gösterir.

### **Kimliğe göre Visio Sayfa Nesnesi Alma**
Bu örnek şu şekilde çalışır:

1. Diagram sınıfından bir nesne oluşturun.
1. Diagram.Pages sınıfının getPage yöntemini çağırın.

Aşağıdaki örnek, Visio çiziminden kimliğe göre bir sayfa nesnesinin nasıl alınacağını gösterir.

#### **Kimliğe Göre Sayfa Nesnesi Al Programlama Örneği**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-GetVisioPagebyID.py" >}}

### **Ada Göre Visio Sayfa Nesnesi Alma**
Bu örnek şu şekilde çalışır:

1. Diagram sınıfından bir nesne oluşturun.
1. Diagram.Pages sınıfının GetPage yöntemini çağırın.

#### **Ada Göre Sayfa Nesnesi Al Programlama Örneği**
Aşağıdaki örnek, Visio çiziminden ada göre bir sayfa nesnesinin nasıl alınacağını gösterir.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-GetVisioPagebyName.py" >}}

## **Bir Visio Sayfasını Başka Bir Diagram'e Kopyalayın**
Python via Java API için Aspose.Diagram, geliştiricilerin içeriğini bir Visio diagram'den diğerine kopyalamasına ve eklemesine olanak tanır. Bu yardım konusu, bu görevin nasıl gerçekleştirileceğini açıklar.

Python via Java API için Aspose.Diagram, bir Visio çizimini temsil eden `Diagram` sınıfına sahiptir. Diagram sınıfı tarafından sunulan Pages özelliği, `Page` nesne koleksiyonunu destekler. PageCollection sınıfı, başka bir Sayfa nesnesi eklemek için çağrılabilen `add` yöntemini gösterir.

Bu örnek şu şekilde çalışır:

1. Diagram sınıfından yeni bir nesne oluşturun.
1. Mevcut bir Visio diagram'i Diagram sınıf nesnesine yükleyin.
1. Yüklenen Visio diagram'den tüm master'ları ekle
1. Yüklenen diagram'den (kopyalanması gereken) sayfa nesnesini alın.
1. Sayfa nesnesi adını ve kimliğini ayarlayın.
1. Yeni diagram'in boş sayfasını kaldırın (isteğe bağlı).
1. PageCollection sınıfının add yöntemini çağırın.
1. Yeni diagram'i bilgisayar belleğine kaydedin.

### **Visio Sayfa Programlama Örneği Kopyalama**
Aşağıdaki kod örneği, bir Visio sayfa nesnesinin başka bir Visio çizimine nasıl kopyalanacağını gösterir.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-CopyVisioPage.py" >}}

## **Visio Sayfasını başka bir Sayfa örneğine kopyalayın**
`Page` sınıfının `copy` yöntemi, klonlamak için bir sayfa örneği alır.

``` python
# import diagram

diagram = Diagram(dataDir + "Drawing1.vsdx")

newPage = Page()

# copy page

newPage.copy(diagram.getPages().getPage("Page-1"))

```

## **Visio Çizimine Boş Sayfa Ekleme**
Python via Java için Aspose.Diagram Microsoft Office Visio çizimine yeni bir boş sayfa ekleyebilir. Bu örnek konuda bunun nasıl yapılacağı açıklanmaktadır.

Pages koleksiyonu tarafından sunulan `add` yöntemi, geliştiricilerin Visio diagram'de yeni bir boş sayfa eklemesine olanak tanır. Sayfa kimliği atanmalıdır.

### **Boş Sayfa Programlama Örneği Ekleme**
Aşağıdaki kod parçası, Visio Çizimine boş bir sayfa ekler:

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-InsertBlankPageInVisio.py" >}}

## **Visio çiziminde Sayfa konumunu taşı**
Python için Aspose.Diagram via Java API Visio çiziminde sayfa konumunu taşıyabilir. `Page` sınıfı tarafından sunulan `moveTo` yöntemi, geliştiricilerin sayfa konumunu taşımasına yardımcı olur.

### **Sayfa konumunu taşı Programlama Örneği**
MoveTo üyesi, Visio çiziminde sayfanın konumunu taşımak için hedef sayfa dizinini parametre olarak alır:

``` python
# import diagram

diagram = Diagram(dataDir + "Drawing1.vsdx")

newPage = Page(1)

# move page in the diagram

newPage.moveTo(2)

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX)
```
