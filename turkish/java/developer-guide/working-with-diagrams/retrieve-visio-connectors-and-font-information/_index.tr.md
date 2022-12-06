---
title: Visio Bağlayıcıları ve Yazı Tipi Bilgilerini Alın
type: docs
weight: 20
url: /tr/java/retrieve-visio-connectors-and-font-information/
---
## **Bağlayıcı Bilgilerini Alma**
 Aspose.Diagram for Java, kimlik ve isim - hakkında bilgi almak için mekanizmalar sağlar[sayfalar](/diagram/tr/java/retrieve-get-copy-and-insert-a-page/) ve[usta](). Ayrıca, şekilleri birbirine bağlayan öğeler olan bağlayıcılar hakkında bilgi almanızı sağlar.

 bu[Bağlamak](https://reference.aspose.com/diagram/java/com.aspose.diagram/connect) nesne, bir Visio çizim sayfasında iki şekli birleştiren bir bağlayıcıyı temsil eder. Tarafından sunulan Connects özelliği[Sayfa](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) class, Aspose.Diagram.Connect nesnelerinin bir koleksiyonunu destekler. Bu özellik, bir bağlayıcı hakkında kimlik ve ad bilgilerini almak için kullanılabilir.

**Aşağıdaki kodun çıktısını gösteren bir konsol penceresi.** 

![yapılacaklar:resim_alternatif_Metin](retrieve-visio-connectors-and-font-information_1.png)
### **Programlama Örneği**
Aşağıdaki kod parçası, bir diagram'deki konektörler için bilgileri alır.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-RetrieveConnectorInfo-RetrieveConnectorInfo.java" >}}
## **Yazı Tipi Bilgilerini Alma**
 Aspose.Diagram, diagram'i oluşturan öğeler hakkında bilgi almak için mekanizmalara sahiptir.[sayfalar](/diagram/tr/java/retrieve-get-copy-and-insert-a-page/), [şablonlar](), [konektörler](https://reference.aspose.com/diagram/java/com.aspose.diagram/ConnectCollection)ve ayrıca yazı tipleri. Bu makale, bir diagram'de hangi yazı tiplerinin kullanıldığını nasıl bulacağınızı gösterir.

 bu[Yazı tipi](https://reference.aspose.com/diagram/java/com.aspose.diagram/font) nesne, bir belgedeki metne uygulanan veya sistemde kullanılabilen bir yazı tipini temsil eder.

Bir Yazı Tipi nesnesi, bir adı (örneğin, "Arial"), Microsoft Visio'in bu yazı tipiyle biçimlendirilmiş metni içeren bir şeklin Karakter bölümündeki Yazı Tipi hücresinde depoladığı yazı tipi kimliğine (örneğin, 3) eşler. Yazı tipi kimlikleri, bir belge farklı sistemlerde açıldığında veya yazı tipleri yüklendiğinde veya kaldırıldığında değişebilir.
### **Yazı Tipi Programlama Örneği Alınıyor**
Aşağıdaki kod parçası, Visio diagram'den yazı tipi bilgilerini alır.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-RetrieveFontInfo-RetrieveFontInfo.java" >}}

![yapılacaklar:resim_alternatif_Metin](retrieve-visio-connectors-and-font-information_2.png)
### **Varsayılan Yazı Tipi Dizinini Alma**
Aspose.Diagram for Java API, Diagram Sınıfının getDefaultFontDir() yöntemini kullanarak varsayılan yazı tipi dizini yolunun alınmasına da izin verir. Aşağıdaki kod parçası, Visio diagram'den varsayılan yazı tipi dizinini alır.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-GetDefaultFontDirectory-GetDefaultFontDirectory.java" >}}
