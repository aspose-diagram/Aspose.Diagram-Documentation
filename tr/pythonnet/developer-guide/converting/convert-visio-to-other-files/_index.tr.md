---
title:  Visio'i diğer formatlara dönüştürün
linktitle:  Visio'i diğer formatlara dönüştürün
type: docs
weight: 40
url: /tr/python-net/convert-visio-to-other-files/
description: Bu konu, Aspose.Diagram'in Visio'i SVG,XPS,XML,XAML biçimlerine dönüştürmeye nasıl izin verdiğini gösterir. VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM'i SVG,XPS,15,0761,XML'ye dönüştürün.
---
## **XML'e Aktar**
### **İhracat Microsoft Visio Çizimi PDF'e**
Kod örnekleri, Microsoft Visio Çiziminin C# kullanılarak PDF'e nasıl aktarılacağını gösterir.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the pdf format
diagram.save("Visio_out.pdf", SaveFileFormat.PDF)
{{< /highlight >}}


 Bu makalede, bir Microsoft Visio diagram kullanarak XML'e nasıl dışa aktarılacağı açıklanmaktadır.[Python via .NET için Aspose.Diagram](https://products.aspose.com/diagram/python-net/) API.

- VDX, bir XML diagram tanımlar.
- VTX, bir XML şablonu tanımlar.
- VSX, bir XML şablonunu tanımlar.

 [Diagram]sınıfı yapıcıları bir diagram'i okur ve Save yöntemi, bir diagram'i farklı bir dosya biçiminde kaydetmek veya dışa aktarmak için kullanılır. Bu makaledeki kod parçacıkları, bir Visio dosyasını şuraya kaydetmek için Kaydet yönteminin nasıl kullanılacağını gösterir:[VDX](https://docs.aspose.com/diagram/python-net/save-visio-document/), [VTX](https://docs.aspose.com/diagram/python-net/save-visio-document/) ve[VSX](https://docs.aspose.com/diagram/python-net/save-visio-document/).

Aşağıdaki resim, aşağıdaki kod parçacıklarında dışa aktarılan diagram'i göstermektedir. Dışa aktarılan dosya, her kod parçacığından önce gösterilir.

|**A Microsoft Visio diagram ihraç edilmek üzere.**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](how-to-convert-a-visio-diagram_3.png)|

### **VSD'i VDX'e aktar**
VDX, diyagramları Microsoft Visio dışındaki ürünlerin okuyabileceği bir biçimde kaydetmenizi sağlayan şema tabanlı bir XML dosya biçimidir. Yazılım uygulamaları arasında diyagramları aktarmak ve düzenlenebilir verileri tutmak için kullanışlı bir formattır.

Bir VSD diagram'i VDX'e aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Visio çizim dosyasını VDX'e yazmak için Diagram sınıfının Save yöntemini çağırın.

|**Dışa aktarılan VDX dosyası.**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](how-to-convert-a-visio-diagram_4.png)|

### **VSD'den VSX'e dışa aktarma**
VSX, diagram'in oluşturulduğu temel nesneler olan şablonları tanımlamak için bir XML formatıdır. Visio dosyası VSX'e dönüştürüldüğünde, yalnızca şablonlar dışa aktarılır.

Bir VSD diagram'i VSX'e aktarmak için:

- Diagram sınıfının bir örneğini oluşturun.
- Visio çizim dosyasını VSX'e yazmak için Diagram sınıfının Save yöntemini çağırın.
### **VSD'i VTX'e aktar**
TVX, bir şablon dosyasının XML temsilidir ve belgenin ayarlarını saklar.

Bir VSD diagram'i VTX'e aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Visio çizim dosyasını VTX biçiminde yazmak için diagram sınıfının Save yöntemini çağırın.
### **Microsoft Visio Çizimi XML'e Aktar**
Kod örnekleri, Microsoft Visio Çiziminin C# kullanılarak XML'e nasıl aktarılacağını gösterir.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the vdx format
diagram.save("Visio_out.vdx", SaveFileFormat.VDX)

#// Save diagram in the vtx format
diagram.save("Visio_out.vtx", SaveFileFormat.VTX)

#// Save diagram in the vsx format
diagram.save("Visio_out.vsx", SaveFileFormat.VSX)
{{< /highlight >}}


## **XPS'e aktar**
 Bu makalede, bir Microsoft Visio diagram'in XPS kullanılarak nasıl dışa aktarılacağı açıklanmaktadır.[Python via .NET için Aspose.Diagram](https://products.aspose.com/diagram/python-net/) API.
diagram dosyalarını okumak için [Diagram]sınıf yapıcısını ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemini kullanın.

Bu makaledeki kod parçacıkları aşağıdaki diagram'i girdi olarak alır. Diğer diagram formatlarını da (VSS, VSSX, VSSM, VDX, VST, VSTX, VDX, VTX veya VSX) kullanabilirsiniz.

|**Kaynak belge.**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](how-to-convert-a-visio-diagram_5.png)|


VSD diagram'i XPS'e dışa aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Diagram sınıfının Save yöntemini çağırın ve çıkış formatı olarak XPS'i ayarlayın.
### **İhracat Microsoft Visio Çizimi XPS'e**
Kod örnekleri, Microsoft Visio Çiziminin C# kullanılarak XPS'e nasıl aktarılacağını gösterir.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the xps format
diagram.save("Visio_out.xps", SaveFileFormat.XPS)
{{< /highlight >}}


## **Diagram'i SVG'e dışa aktarın**
 Bu makalede, bir Microsoft Visio diagram'in SVG'e (Ölçeklenebilir Vektör Grafikleri) kullanılarak nasıl dışa aktarılacağı açıklanmaktadır.[Python via .NET için Aspose.Diagram](https://products.aspose.com/diagram/python-net/) API.

diagram dosyalarını okumak için [Diagram]sınıf yapıcısını ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemini kullanın.

VSD diagram'i SVG'e aktarmak için aşağıdaki adımları gerçekleştirin:

1. Diagram sınıfının bir örneğini oluşturun.
1. Sınıfın Save yöntemini çağırın ve dışa aktarma formatı olarak SVG'i ayarlayın.
### **İhracat Microsoft Visio Çizimi SVG'e**
Kod örnekleri, C# kullanarak bir diagram'in SVG'e nasıl aktarılacağını gösterir.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the svg format
diagram.save("Visio_out.svg", SaveFileFormat.SVG)
{{< /highlight >}}


Bir Visio çizimini seçici şekillerle dışa aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Ayarları burada anlatıldığı gibi belirtmek için herhangi bir SaveOption sınıfının bir örneğini oluşturun:[Visio Kaydetme Seçeneklerini Belirtin](https://docs.aspose.com/diagram/python-net/save-visio-document/#specifying-visio-save-options)
1. Diagram sınıf nesnesinin Kaydetme yöntemini çağırın ve kaydetme seçeneği sınıf nesnesini parametre olarak iletin.
### **Dönüştür Visio Seçici Şekillerle Çizim Programlama Örneği**
Kod örneği, bir çizimin seçici Visio şekillerle nasıl dışa aktarılacağını gösterir.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

options = saving.SVGSaveOptions()
shapes = options.shapes;
#// get shapes by page index and shape ID, and then add in the shape collection object
shapes.add(diagram.pages[0].shapes.get_shape(1));
shapes.add(diagram.pages[0].shapes.get_shape(2));
    
#// Save one page only, by page index
options.page_index = 0
    
#// Save resultant svg file
diagram.save("ExportToSvg_out.svg", options)
{{< /highlight >}}
