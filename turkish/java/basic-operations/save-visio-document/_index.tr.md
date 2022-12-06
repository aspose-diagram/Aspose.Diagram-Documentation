---
title: Visio belgesini programlı olarak kaydedin
linktitle: Visio belgesini kaydet
type: docs
weight: 30
url: /tr/java/save-visio-document/
description: Bu sayfada Visio belgesinin dosyaya nasıl kaydedileceği, Aspose.Diagram kitaplığıyla akış nasıl açıklanır.
---
## **Visio Çizim Kaydet Genel Bakış**
 Kullan[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\) bir Microsoft Visio çizimini kaydetme yöntemi. Bir çizimi dosyaya kaydetmeye izin veren aşırı yüklemeler vardır. Çizim, Aspose.Diagram tarafından desteklenen herhangi bir kaydetme biçiminde kaydedilebilir. Desteklenen tüm kaydetme biçimlerinin listesi için bkz.[Dosya Biçimini Kaydet](https://reference.aspose.com/diagram/java/com.aspose.diagram/SaveFileFormat) Sıralama.
## **Kaydediliyor Visio Diagram**
 Aspose.Diagram API'in Diagram sınıfı, bir Visio çizimini temsil eder ve geliştiriciler, Visio diagram nesnesini desteklenen herhangi bir dosya biçiminde kaydedebilir. Microsoft Visio dosyasını kaydetmek için[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\)) yöntemi, tam yol veya bir dosya akış nesnesi olan bir dosya adını kabul eder. Aspose.Diagram API, dosya uzantısından kaydetme biçimini çıkarır ve ayrıca çıktı dosyası biçimini belirtmek için ek bir SaveFileFormat parametresi sunar.
### **Visio Diagram'i herhangi bir Desteklenen Dosya Formatında kaydedin**
Geliştiriciler, Aspose.Diagram API'i kullanarak bir Visio diagram'i aşağıda listelenen desteklenen herhangi bir dosya biçiminde kaydedebilir:
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG and XAML**
### **Diagram Programlama Örneği kaydediliyor**
Aşağıdaki örnek, bir belgeyi bir dosyaya kaydeder.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-SaveVisioDiagram-SaveVisioDiagram.java" >}}
## **Visio Kaydetme Seçeneklerini Belirleme**
 Bir kaç tane var[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\)bir SaveOptions nesnesini kabul eden yöntem aşırı yüklemeleri. Bu, SaveOptions sınıfından türetilen bir sınıfın nesnesi olmalıdır. Her kaydetme biçiminin, o kaydetme biçimi için kaydetme seçeneklerini tutan karşılık gelen bir sınıfı vardır; örneğin, SaveFileFormat.PDF kaydetme biçimi için PdfSaveOptions vardır.
### **Visio Diagram Kaydetme Seçenekleri**
Bu örnekler şunların nasıl yapılacağını gösterir:

- [Diagram Kaydetme Seçeneklerini Kullanın](/diagram/tr/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [PDF Kaydetme Seçeneklerini Kullanın](/diagram/tr/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [HTML Kaydetme Seçeneklerini Kullanın](/diagram/tr/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Görüntü Kaydetme Seçeneklerini Kullanın](/diagram/tr/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [SVG Kaydetme Seçeneklerini Kullanın](/diagram/tr/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
#### **Diagram Kaydetme Seçeneklerinin Kullanımı**
Aşağıdaki kod, bir belgeyi Visio biçiminde kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseDiagramSaveOptions-UseDiagramSaveOptions.java" >}}



#### **PDF Kaydetme Seçeneklerinin Kullanımı**
Aşağıdaki kod, bir belgeyi PDF biçiminde kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-UsePDFSaveOptions.java" >}}



#### **HTML Kaydetme Seçeneklerinin Kullanımı**
Aşağıdaki kod, bir belgeyi HTML biçiminde kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseHTMLSaveOptions-UseHTMLSaveOptions.java" >}}



#### **Görüntü Kaydetme Seçeneklerinin Kullanımı**
Aşağıdaki kod, bir belgeyi görüntü biçiminde kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseImageSaveOptions-UseImageSaveOptions.java" >}}
#### **SVG Kaydetme Seçeneklerinin Kullanımı**
Aşağıdaki kod, bir belgeyi SVG biçiminde kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseSVGSaveOptions-UseSVGSaveOptions.java" >}}
