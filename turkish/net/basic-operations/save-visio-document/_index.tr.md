---
title: Visio belgesini programlı olarak kaydedin
linktitle: Visio belgesini kaydet
type: docs
weight: 30
url: /tr/net/save-visio-document/
description: Bu sayfada Visio belgesinin dosyaya nasıl kaydedileceği, Aspose.Diagram kitaplığıyla akış nasıl açıklanır.
---
## **Visio Çizim Kaydet Genel Bakış**
 Kullan[Diagram.Save]() Microsoft Visio çizimini kaydetme yöntemi. Bir çizimi dosyaya kaydetmeye izin veren aşırı yüklemeler vardır. Çizim, Aspose.Diagram tarafından desteklenen herhangi bir kaydetme biçiminde kaydedilebilir. Desteklenen tüm kaydetme biçimlerinin listesi için bkz.[Dosya Biçimini Kaydet]() Sıralama.
## **Kaydediliyor Visio Diagram**
 Aspose.Diagram API'in Diagram sınıfı, bir Visio çizimini temsil eder ve geliştiriciler, Visio diagram nesnesini desteklenen herhangi bir dosya biçiminde kaydedebilir. Microsoft Visio dosyasını kaydetmek için[Diagram.Save]()yönteminde, tam yolu olan bir dosya adını veya bir dosya akış nesnesini kabul eder. Aspose.Diagram API, dosya uzantısından kaydetme biçimini çıkarır ve ayrıca çıktı dosyası biçimini belirtmek için ek bir SaveFileFormat parametresi sunar.
### **Visio Diagram'i herhangi bir Desteklenen Dosya Formatında kaydedin**
Geliştiriciler, Aspose.Diagram API'i kullanarak bir Visio diagram'i aşağıda listelenen desteklenen herhangi bir dosya biçiminde kaydedebilir:
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG, SWF and XAML**
### **Diagram Programlama Örneği kaydediliyor**
Aşağıdaki örnek, bir belgeyi bir dosyaya kaydeder.

{{< highlight "java" >}}

 // Save a Visio diagram

diagram.Save(GetMyDir() + "MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Visio Kaydetme Seçeneklerini Belirleme**
 Bir kaç tane var[Diagram.Save]() bir SaveOptions nesnesini kabul eden yöntem aşırı yüklemeleri. Bu, SaveOptions sınıfından türetilen bir sınıfın nesnesi olmalıdır. Her kaydetme biçimi, o kaydetme biçimi için kaydetme seçeneklerini tutan karşılık gelen bir sınıfa sahiptir. Örneğin, SaveFileFormat.PDF kaydetme biçimi için PdfSaveOptions vardır.
### **Visio Diagram Kaydetme Seçenekleri**
Bu örnekler şunların nasıl yapılacağını gösterir:

- [Diagram Kaydetme Seçeneklerini Kullanın](https://docs.aspose.com/diagram/net/save-visio-document/).
- [PDF Kaydetme Seçeneklerini Kullanın](https://docs.aspose.com/diagram/net/save-visio-document/).
- [HTML Kaydetme Seçeneklerini Kullanın](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Görüntü Kaydetme Seçeneklerini Kullanın](https://docs.aspose.com/diagram/net/save-visio-document/).
- [SVG Kaydetme Seçeneklerini Kullanın](https://docs.aspose.com/diagram/net/save-visio-document/).
- [SWF Kaydetme Seçeneklerini Kullanın](https://docs.aspose.com/diagram/net/save-visio-document/).
#### **Diagram Kaydetme Seçeneklerinin Kullanımı**
Aşağıdaki kod, bir belgeyi Visio biçiminde kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseDiagramSaveOptions-UseDiagramSaveOptions.cs" >}}



#### **PDF Kaydetme Seçeneklerinin Kullanımı**
Aşağıdaki kod, bir belgeyi PDF biçiminde kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-UsePDFSaveOptions.cs" >}}



#### **HTML Kaydetme Seçeneklerinin Kullanımı**
Aşağıdaki kod, bir belgeyi HTML dosya biçiminde kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseHTMLSaveOptions-UseHTMLSaveOptions.cs" >}}



#### **Görüntü Kaydetme Seçeneklerinin Kullanımı**
Aşağıdaki kod, bir belgeyi görüntü dosyası biçiminde kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.



{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseImageSaveOptions-UseImageSaveOptions.cs" >}}


SVG Kaydetme Seçeneklerinin Kullanımı

Aşağıdaki kod, bir belgeyi SVG biçiminde kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseSVGSaveOptions-UseSVGSaveOptions.cs" >}}


SWF Kaydetme Seçeneklerinin Kullanımı

Aşağıdaki kod, bir belgeyi SWF biçiminde kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseSWFSaveOptions-UseSWFSaveOptions.cs" >}}

Bazen, geliştiricilerin Visio diyagramlarını programlı olarak farklı dosya biçimlerine kaydetmesi veya dışa aktarması gerekir (VDX, PDF, JPEG vb.).
## **VSD dosyasını farklı dosya biçimlerine kaydedin (VDX, PDF ve JPEG)**
 Bu makale, nasıl kullanılacağını gösteren bir kod örneği sağlar.[VSTO](https://docs.aspose.com/diagram/net/save-visio-document/) ve[Aspose.Diagram for .NET](https://docs.aspose.com/diagram/net) Microsoft Visio VSD dosyasını VDX dosyasına, PDF dosyasına veya JPEG dosyasına programlı olarak kaydetmek için. Aşağıda, bir VSD dosyasının farklı dosya biçimlerine nasıl kaydedileceğini açıklayan VSTO ve Aspose.Diagram for .NET için paralel kod parçacıkları bulunmaktadır. Aspose.Diagram kodunun daha kısa olduğunu fark edeceksiniz. Kodu kullanmaktan ve özel ihtiyaçlarınızı karşılamak için değiştirmekten çekinmeyin.
### **VSD Dosyasını VSTO ile Diğer Formatlara Kaydetme**
VSTO, Microsoft Visio dosyalarıyla programlama yapmanızı sağlar. Bir dosyayı başka formatlara kaydetmek için:

1. Bir Visio uygulama nesnesi oluşturun.
1. Uygulama nesnesini görünmez yapın.
1. diagram'i yükleyin.
1. VDX, PDF ve JPEG'e kaydedin.
1. Visio uygulama nesnesinden çıkın.
#### **VSD Dosyasını VSTO Programlama Örneğiyle Kaydetme**
{{% alert color="primary" %}} 

Visio = Microsoft.Office.Interop.Visio kullanarak;
İthalatlar Visio = Microsoft.Office.Interop.Visio

{{% /alert %}} 

**Örnek:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-SaveDiagramTo-VDX-PDF-JPEG-withVSTO-SaveDiagramTo_VDX_PDF_JPEG_withVSTO.cs" >}}
### ` `**VSD Dosyasını Aspose.Diagram for .NET İle Diğer Formatlara Kaydetmek**
Aspose.Diagram kullanarak geliştiriciler makinede Microsoft Office Visio'e ihtiyaç duymazlar ve Microsoft Office Otomasyondan bağımsız çalışabilirler.

Aşağıdaki kod parçacıkları şunların nasıl yapıldığını gösterir:

1. diagram yükleyin.
1. diagram'i VSX, PDF ve JPEG'e kaydedin.
#### **VSD Dosyasını Aspose.Diagram for .NET Programlama Örneği ile Kaydetme**
{{% alert color="primary" %}} 

Aspose.Diagram kullanarak;
İthal Aspose.Diagram

{{% /alert %}} 

**Örnek:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-SaveDiagramTo-VDX-PDF-JPEG-withAspose-SaveDiagramTo_VDX_PDF_JPEG_withAspose.cs" >}}
