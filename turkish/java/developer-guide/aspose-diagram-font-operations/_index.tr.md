---
title: Aspose.Diagram Yazı Tipi İşlemleri
type: docs
weight: 170
url: /tr/java/aspose-diagram-font-operations/
---
{{% alert color="primary" %}} 

Aspose.Diagram, geliştiricilerin Visio diyagramlarında işleme için yazı tipi dizinlerini ayarlamasına olanak tanır. Bu makale, özel dizinlerdeki yazı tiplerinin nasıl kullanılacağını gösterir.

{{% /alert %}} 
### **Yazı Tipleriyle Çalışmak**
#### **Aspose.Diagram, Windows'de TrueType Yazı Tiplerini Aradığı Yer**
 Aspose.Diagram, içinde yazı tiplerini arar.**Windows\Yazı Tipleri** dosya. Bu varsayılan ayar çoğu zaman çalışır, bu nedenle yalnızca gerçekten ihtiyacınız varsa kendi yazı tipi klasörlerinizi belirtin.
#### **Yazı Tipi Klasörünü Açıkça Belirtme**
 Aspose.Diagram API'ler, setFontDirs yöntemini kullanıma sundu.[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) yazı tipi klasörlerini aşağıda açıklandığı gibi belirtmek için class.

1. Diagram.setFontDirs yöntemi, bir dize dizisini parametre olarak alır, dolayısıyla geliştirici bu yaklaşımı kullanarak birçok yazı tipi dizini belirtebilir.

{{% alert color="primary" %}} 

Yukarıda belirtilen yaklaşımı kullanarak yazı tipi klasörünü belirtirken, yazı tipi konumunu uygulamanın başında ayarlamanızı öneririz, aksi takdirde kötü biçimlendirilmiş sonuçlar alabilirsiniz.

{{% /alert %}} {{% alert color="primary" %}} 

Yazı tipleri klasörünün yukarıdaki yöntemlerden herhangi biri kullanılarak ayarlanması, Aspose.Diagram API'in yazı tiplerini sistemin yazı tipi klasörü gibi varsayılan konumlarda aramayacağını garanti etmez.

{{% /alert %}} 

Aspose.Diagram'in yazı tiplerini işlerken veya katıştırırken TrueType yazı tiplerini birden çok klasörde arayacak şekilde nasıl ayarlanacağını gösterir.
#### **Programlama Örneği**
Aşağıdaki kod örneği, yazı tiplerini işlerken veya katıştırırken TrueType yazı tiplerini birden çok klasörde aramak için Aspose.Diagram'in nasıl ayarlanacağını gösterir.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Fonts-SpecifyFontLocation-SpecifyFontLocation.java" >}}
### **İşleme Sırasında Eksik Yazı Tipleri ve Yazı Tipi Değiştirme Bildirimi Alın**
Aspose.Diagram API, çizimi düzgün bir şekilde PDF formatına dönüştürmek için doğru yazı tipine erişim gerektirir. Gerekli yazı tipi makinede yoksa, Aspose.Diagram API, varsayılan yazı tipini veya makinedeki mevcut en yakın yazı tipini kullanarak bu yazı tipinin herhangi bir örneğini oluşturur, çünkü bu değişiklik işlenmiş çizimin görünümünü değiştirebilir, geliştiricilerin bir yazı tipi eksik olduğunda ve hangi yazı tipiyle değiştirileceği bildirilir.
#### **Eksik Font Bildirimi ve Font Değiştirme Programlama Örneği**
Oluşturma sırasında yazı tipi değişikliği konusunda bilgilendirilmek için:

1. uygulayan bir sınıf oluşturun.[IUyarıGeri Arama](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback)
1. PdfSaveOptions.setWarningCallback(com.aspose.diagram.IWarningCallback) özelliğine iletin.

Çizimin kaydedilmesi sırasında örneğin[IUyarıGeri Arama](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback)çizimle ilgili herhangi bir potansiyel aslına uygunluk sorunu varsa çağrılır. Bu durumda, yalnızca yazı tipi değişikliği olan uyarıları işlemeyi ve uyarıyı ekrana yazdırmayı seçiyoruz. Aşağıdaki örnek, kullanarak yazı tipi değiştirme bildirimlerinin nasıl alınacağını gösterir.[IUyarıGeri Arama](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback).

**Java**

{{< highlight "java" >}}

 // load the document to render.

Diagram diagram = new Diagram("C:\\temp\\Output.vsdx");


// initialize PdfSaveOptions object

com.aspose.diagram.PdfSaveOptions saveOp = new com.aspose.diagram.PdfSaveOptions();

// create a new class implementing IWarningCallback which collect any warnings produced during drawing save.

HandleDocumentWarnings callback = new HandleDocumentWarnings();

saveOp.setWarningCallback(callback);



// pass the save options along with the save path to the save method.

diagram.save("C:\\temp\\Rendering.MissingFontNotification Out.pdf", saveOp);

{{< /highlight >}}
#### **IWarningCallback'i uygulama**
Son adım, şu komutu uygulayan sınıfı oluşturmaktır:[IUyarıGeri Arama](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback)arayüz. Bu sınıf, yazı tipi değiştirme uyarılarını konsola yazdıracaktır. Aşağıdaki örnek, belge kaydetme sırasında herhangi bir yazı tipi değişikliğinden haberdar olmak için IWarningCallback'in nasıl uygulanacağını gösterir.



**Java**

{{< highlight "java" >}}

 public class HandleDocumentWarnings implements IWarningCallback {

     /**

     * Our callback only needs to implement the "Warning" method. This method is

     * called whenever there is a potential issue during document processing.

     * The callback can be set to listen for warnings generated during document

     * load and/or document save.

     */

     public void warning(WarningInfo info) {

         // We are only interested in fonts being substituted.

         if (info.getWarningType() == WarningType.FONT_SUBSTITUTION) {

         System.out.println("Font substitution: " + info.getDescription());

     }

 }

}

{{< /highlight >}}
