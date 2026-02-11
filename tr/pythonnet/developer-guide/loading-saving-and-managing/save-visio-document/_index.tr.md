---
title: Visio belgesini programlı olarak kaydedin
linktitle: Visio belgesini kaydet
type: docs
weight: 30
url: /tr/python-net/save-visio-document/
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

- [Diagram Kaydetme Seçeneklerini Kullanın](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [PDF Kaydetme Seçeneklerini Kullanın](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [HTML Kaydetme Seçeneklerini Kullanın](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Görüntü Kaydetme Seçeneklerini Kullanın](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [SVG Kaydetme Seçeneklerini Kullanın](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [SWF Kaydetme Seçeneklerini Kullanın](https://docs.aspose.com/diagram/python-net/save-visio-document/).
#### **Diagram Kaydetme Seçeneklerinin Kullanımı**
Aşağıdaki kod, bir belgeyi Visio biçiminde kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

options = saving.DiagramSaveOptions(SaveFileFormat.VSDX)

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", options)
{{< /highlight >}}




#### **PDF Kaydetme Seçeneklerinin Kullanımı**
Aşağıdaki kod, bir belgeyi PDF biçiminde kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
options = saving.PdfSaveOptions()
    
#// Save one page only, by page index
options.page_index = 0

#// Save diagram in the pdf format
diagram.save("CreateNewVisio_out.pdf", options)
{{< /highlight >}}




#### **HTML Kaydetme Seçeneklerinin Kullanımı**
Aşağıdaki kod, bir belgeyi HTML dosya biçiminde kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
options = saving.HTMLSaveOptions()
    
#// Save one page only, by page index
options.page_index = 0

#// Save diagram in the html format
diagram.save("Visio_out.html", options)
{{< /highlight >}}




#### **Görüntü Kaydetme Seçeneklerinin Kullanımı**
Aşağıdaki kod, bir belgeyi görüntü dosyası biçiminde kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.




{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
#// Save diagram as PNG
options = saving.ImageSaveOptions(SaveFileFormat.PNG)
    
#// Save one page only, by page index
options.page_index = 0

#// Save diagram in the png format
diagram.save("ExportPageToImage_out.png", options)
{{< /highlight >}}



SVG Kaydetme Seçeneklerinin Kullanımı

Aşağıdaki kod, bir belgeyi SVG biçiminde kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
#// Save diagram as svg
options = saving.SVGSaveOptions()
    
#// Save one page only, by page index
options.page_index = 0

#// Save diagram in the svg format
diagram.save("ExportPageToSvg_out.svg", options)
{{< /highlight >}}


Bazen, geliştiricilerin Visio diyagramlarını programlı olarak farklı dosya biçimlerine kaydetmesi veya dışa aktarması gerekir (VDX, PDF, JPEG vb.).

### ` `**VSD Dosyasını Python via .NET için Aspose.Diagram ile Diğer Formatlara Kaydetme**
Aspose.Diagram kullanarak geliştiriciler makinede Microsoft Office Visio'e ihtiyaç duymazlar ve Microsoft Office Otomasyondan bağımsız çalışabilirler.

Aşağıdaki kod parçacıkları şunların nasıl yapıldığını gösterir:

1. diagram yükleyin.
1. diagram'i VSX, PDF ve JPEG'e kaydedin.
#### **Python via .NET Programlama Örneği için VSD Dosyasını Aspose.Diagram ile Kaydetme**
{{% alert color="primary" %}} 

aspose.diagram'i içe aktar
aspose.diagram'den içe aktarma *

{{% /alert %}} 

**Örnek:**


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
#// Save the diagram as VDX
vsdDiagram.save(os.path.join(outputDir, "SaveDiagramToVDXwithAspose_out.vdx"), SaveFileFormat.VDX)

#// Save as PDF
vsdDiagram.save(os.path.join(outputDir, "SaveDiagramToPDFwithAspose_out.pdf"), SaveFileFormat.PDF)

#// Save as JPEG
vsdDiagram.save(os.path.join(outputDir, "SaveDiagramToJPGwithAspose_out.jpg"), SaveFileFormat.JPEG)
{{< /highlight >}}

