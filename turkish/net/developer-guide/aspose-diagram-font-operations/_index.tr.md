---
title: Aspose.Diagram Yazı Tipi İşlemleri
type: docs
weight: 180
url: /tr/net/aspose-diagram-font-operations/
description: Bu sayfada, Aspose.Diagram kitaplığıyla yazı tiplerinin nasıl değiştirileceği açıklanmaktadır.
---
## **TrueType Yazı Tiplerinin Konumu Nasıl Belirlenir?**
Aspose.Diagram, geliştiricilerin Visio diyagramlarında işleme için yazı tipi dizinlerini ayarlamasına olanak tanır. Bu makale, özel dizinlerdeki yazı tiplerinin nasıl kullanılacağını gösterir.
### **Yazı Tipleriyle Çalışmak**
#### **Aspose.Diagram, Windows'de TrueType Yazı Tiplerini Aradığı Yer**
 Aspose.Diagram, içinde yazı tiplerini arar.**Windows\Yazı Tipleri** dosya. Bu varsayılan ayar çoğu zaman çalışır, bu nedenle yalnızca gerçekten ihtiyacınız varsa kendi yazı tipi klasörlerinizi belirtin.
#### **Yazı Tipi Klasörünü Açıkça Belirtme**
Aspose.Diagram API'ler, için FontDirs özelliğini kullanıma sundu[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) yazı tipi klasörlerini aşağıda açıklandığı gibi belirtmek için class.

1. Diagram.FontDirs özelliği bir dize dizisini kabul eder, böylece geliştirici bu yaklaşımı kullanarak birçok yazı tipi dizini belirtebilir.

{{% alert color="primary" %}} 

Yukarıda belirtilen yaklaşımı kullanarak yazı tipi klasörünü belirtirken, yazı tipi konumunu uygulamanın başında ayarlamanızı öneririz, aksi takdirde kötü biçimlendirilmiş sonuçlar alabilirsiniz.

{{% /alert %}} {{% alert color="primary" %}} 

Yazı tipleri klasörünün yukarıdaki yöntemlerden herhangi biri kullanılarak ayarlanması, Aspose.Diagram API'in yazı tiplerini sistemin yazı tipi klasörü gibi varsayılan konumlarda aramayacağını garanti etmez.

{{% /alert %}} 
#### **Programlama Örneği**
Aşağıdaki kod örneği, yazı tiplerini işlerken veya katıştırırken TrueType yazı tiplerini birden çok klasörde aramak için Aspose.Diagram'in nasıl ayarlanacağını gösterir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-OS-Fonts-Location-SpecifyFontLocation-SpecifyFontLocation.cs" >}}
### **İşleme Sırasında Eksik Yazı Tipleri ve Yazı Tipi Değiştirme Bildirimi Alın**
Aspose.Diagram API, çizimi düzgün bir şekilde PDF formatına dönüştürmek için doğru yazı tipine erişim gerektirir. Gerekli yazı tipi makinede yoksa, Aspose.Diagram API, varsayılan yazı tipini veya makinedeki mevcut en yakın yazı tipini kullanarak bu yazı tipinin herhangi bir örneğini oluşturur, çünkü bu değişiklik işlenmiş çizimin görünümünü değiştirebilir, geliştiricilerin bir yazı tipi eksik olduğunda ve hangi yazı tipiyle değiştirileceği bildirilir.
#### **Eksik Font Bildirimi ve Font Değiştirme Programlama Örneği**
Oluşturma sırasında yazı tipi değişikliği konusunda bilgilendirilmek için:

1. uygulayan bir sınıf oluşturun.[IUyarıGeri Arama](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback)
1. PdfSaveOptions.WarningCallback özelliğine iletin.

Çizimin kaydedilmesi sırasında örneğin[IUyarıGeri Arama](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback)çizimle ilgili herhangi bir potansiyel aslına uygunluk sorunu varsa çağrılır. Bu durumda, yalnızca yazı tipi değişikliği olan uyarıları işlemeyi ve uyarıyı ekrana yazdırmayı seçiyoruz. Aşağıdaki örnek, kullanarak yazı tipi değiştirme bildirimlerinin nasıl alınacağını gösterir.[IUyarıGeri Arama](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback).

**C#**

{{< highlight "java" >}}

 // The path to the documents directory.

string dataDir = RunExamples.GetDataDir_Intro();

// load the document to render.

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// initialize PdfSaveOptions object

PdfSaveOptions saveOp = new PdfSaveOptions();

// create a new class implementing IWarningCallback which collect any warnings produced during drawing save.

HandleDocumentWarnings callback = new HandleDocumentWarnings();

saveOp.WarningCallback = callback;

// pass the save options along with the save path to the save method.

diagram.Save(dataDir + "NotificationofMissingFonts_Out.pdf", saveOp);

{{< /highlight >}}
#### **IWarningCallback'i uygulama**
Son adım, şu komutu uygulayan sınıfı oluşturmaktır:[IUyarıGeri Arama](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback)arayüz. Bu sınıf, yazı tipi değiştirme uyarılarını konsola yazdıracaktır. Aşağıdaki örnek, belge kaydetme sırasında herhangi bir yazı tipi değişikliğinden haberdar olmak için IWarningCallback'in nasıl uygulanacağını gösterir.

**C#**

{{< highlight "java" >}}

 class HandleDocumentWarnings : IWarningCallback

{

    /**

    * Our callback only needs to implement the "Warning" method. This method is

    * called whenever there is a potential issue during document processing.

    * The callback can be set to listen for warnings generated during document

    * load and/or document save.

    */

    public void Warning(WarningInfo info)

    {

        // We are only interested in fonts being substituted.

        if (info.WarningType == WarningType.FontSubstitution)

        {

            Console.WriteLine("Font substitution: " + info.Description);

        }

    }

}

{{< /highlight >}}
