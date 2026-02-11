---
title: Yönlendirmeyi Ayarlayın ve Kaydederken Gizli Visio Sayfalarının Dışa Aktarılmasını Kontrol Edin
type: docs
weight: 20
url: /tr/python-java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
---
## **Visio Sayfa Düzenini Dikey veya Yatay olarak değiştirme**
Python via Java API için Aspose.Diagram, geliştiricilerin Visio çizim sayfasının yönünü programlı olarak ayarlamasına olanak tanır. Bu yardım konusu, bu görevin nasıl gerçekleştirileceğini açıklar.

Python via Java API için Aspose.Diagram, bir Visio çizim sayfasını temsil eden `Page` sınıfına sahiptir. Page sınıfı tarafından sunulan PageSheet özelliği ayrıca yazdırma özelliklerini de gösterir. Yazdırma özelliklerinin `PrintPageOrientation` alanı, sayfanın döndürülmesine izin verir. Dikey, Yatay ve yazıcıdaki ile aynı olmak üzere üç seçenek sunar. PrintPageOrientation alanı, Python via Java API için Aspose.Diagram kullanılarak programlı olarak ayarlanabilir.

Bu örnek şu şekilde çalışır:

1. Mevcut bir Visio diagram'i Diagram sınıf nesnesine yükleyin.
1. Visio sayfasını ayıklayın
1. Yönünü Dikey, Yatay veya yazıcıdakiyle aynı olarak ayarlayın.
1. Visio diagram'i kaydedin.

### **Oryantasyon Programlama Örneği Ayarla**
Aşağıdaki kod örneği, Visio sayfasının yönünün nasıl ayarlanacağını gösterir.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# initialize the new visio diagram
diagram = Diagram("DrawingFlowCharts.vsdx")

# get Visio page
page = diagram.getPages().getPage("Flow 1")
# page orientation
page.getPageSheet().getPrintProps().getPrintPageOrientation().setValue(PrintPageOrientationValue.LANDSCAPE)
# save Visio
diagram.save("SetPageOrientation_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```

## **Kaydederken Gizli Visio Sayfalarının Dışa Aktarılmasını Kontrol Edin**
Aspose.Diagram Python için via Java API, geliştiricilerin tasarruf Visio sayfa dahil etmesine veya hariç tutulmasına izin verir. Hatta Python via Java API için Aspose.Diagram'i kullanarak Visio sayfayı gizleyebilirler çünkü seçeneği ShapeSheet sayfasındaki UIVisibility hücresi aracılığıyla zaten mevcuttur.

### **Visio Diagram'de bir Sayfayı Gizle ve Dışa Aktarma Seçeneğini Ayarla**
Python via Java API için Aspose.Diagram, bir Visio çizim sayfasını temsil eden `Page` sınıfına sahiptir. Page sınıfı tarafından sunulan PageSheet özelliği, sayfa özelliklerini de gösterir. Sayfa özelliklerinin `UIVisibility` alanı, sayfanın gizlenmesine izin verir. Geliştiriciler daha sonra `SVGSaveOptions`, `XPSSaveOptions`, `ImageSaveOptions`, `HTMLSaveOptions` ve `PdfSaveOptions` sınıflarına eklenen `exportHiddenPage` özelliğini kullanabilir.

#### **PDF için Dışa Aktarma Seçeneğini ayarlayın**
Aşağıdaki kod, diagram - PDF biçimini kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")
        
# load an existing Visio
diagram = Diagram("DrawingFlowCharts.vsdx")
# get a particular page
page = diagram.getPages().getPage("Flow 2")
# set Visio page visibility
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE)

# initialize PDF save options
options = PdfSaveOptions()
# set export option of hidden Visio pages
options.setExportHiddenPage(False)

# Save the Visio diagram
diagram.save("ExportOfHiddenVisioPagesToPDF_Out.pdf", options)

jpype.shutdownJVM()

{{< /highlight >}}
```

#### **HTML için Dışa Aktarma Seçeneğini ayarlayın**
Aşağıdaki kod, diagram - HTML biçimini kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load an existing Visio
diagram = Diagram("DrawingFlowCharts.vsdx")
# get a particular page
page = diagram.getPages().getPage("Flow 2")
# set Visio page visibility
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE)

# initialize PDF save options
options = HTMLSaveOptions()
# set export option of hidden Visio pages
options.setExportHiddenPage(False)
# set export option of comments
options.setExportComments(False)
# Save the Visio diagram
diagram.save("ExportOfHiddenVisioPagesToHTML_Out.html", options)

jpype.shutdownJVM()

{{< /highlight >}}
```

#### **Görüntü için Dışa Aktarma Seçeneğini Ayarlayın**
Aşağıdaki kod, bir diagram'i görüntü formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load an existing Visio
diagram = Diagram("DrawingFlowCharts.vsdx")
# get a particular page
page = diagram.getPages().getPage("Flow 2")
# set Visio page visibility
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE)
# initialize PDF save options
options = ImageSaveOptions(SaveFileFormat.JPEG)
# set export option of hidden Visio pages
options.setExportHiddenPage(False)
# set export option of comments
options.setExportComments(False)

# Save the Visio diagram
diagram.save("ExportOfHiddenVisioPagesToImage_Out.jpeg", options)

jpype.shutdownJVM()

{{< /highlight >}}
```

#### **SVG için Dışa Aktarma Seçeneğini ayarlayın**
Aşağıdaki kod, diagram - SVG biçimini kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load an existing Visio
diagram = Diagram("DrawingFlowCharts.vsdx")
# get a particular page
page = diagram.getPages().getPage("Flow 2")
# set Visio page visibility
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE)

# initialize PDF save options
options = SVGSaveOptions()
# set export option of hidden Visio pages
options.setExportHiddenPage(False)
# Set SVG fit to view port
options.setSVGFitToViewPort(True)
# Set export element as Rectangle
options.setExportElementAsRectTag(True)

# save the Visio diagram
diagram.save("ExportOfHiddenVisioPagesToSVG_Out.svg", options)

jpype.shutdownJVM()

{{< /highlight >}}
```
