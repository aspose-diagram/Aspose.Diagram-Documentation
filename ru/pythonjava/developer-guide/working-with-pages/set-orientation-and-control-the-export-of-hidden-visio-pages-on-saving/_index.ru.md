---
title: Установка ориентации и управление экспортом скрытых Visio страниц при сохранении
type: docs
weight: 20
url: /ru/python-java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
---
## **Измените макет страницы Visio на книжный или альбомный**
Aspose.Diagram для Python via Java API позволяет разработчикам программно устанавливать ориентацию страницы чертежа Visio. В этом разделе справки объясняется, как выполнить эту задачу.

Aspose.Diagram для Python via Java API имеет класс `Page`, который представляет страницу чертежа Visio. Свойство PageSheet, предоставляемое классом Page, также предоставляет свойства печати. Поле `PrintPageOrientation` свойств печати позволяет поворачивать страницу. Он предлагает три варианта: портретный, альбомный и такой же, как на принтере. Поле PrintPageOrientation можно задать программно, используя Aspose.Diagram вместо Python via Java API.

Этот пример работает следующим образом:

1. Загрузите существующий Visio diagram в объект класса Diagram.
1. Извлечь страницу Visio
1. Установите его ориентацию как Книжная, Альбомная или такая же, как на принтере.
1. Сохраните номер Visio diagram.

### **Пример программирования установки ориентации**
В приведенном ниже примере кода показано, как установить ориентацию страницы Visio.

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

## **Управление экспортом скрытых Visio страниц при сохранении**
Aspose.Diagram для Python via Java API позволяет разработчикам включать или исключать скрытые Visio страницы на сохранении diagram до PDF, HTML, изображение (0761934881, HTML, изображение (0761934881, HTML, изображение (0761934881, HTML, изображение (0761934881, HTML, Image. Даже они могут скрыть страницы Visio, используя Aspose.Diagram для Python via Java API, потому что эта опция уже доступна через ячейку UIVisibility на странице ShapeSheet.

### **Скрыть страницу в Visio Diagram и установить параметр экспорта**
Aspose.Diagram для Python via Java API имеет класс `Page`, который представляет страницу чертежа Visio. Свойство PageSheet, предоставляемое классом Page, также предоставляет свойства страницы. Поле `UIVisibility` в свойствах страницы позволяет скрыть страницу. Затем разработчики могут использовать свойство `exportHiddenPage`, которое добавляется в классы `SVGSaveOptions`, `XPSSaveOptions`, `ImageSaveOptions`, `HTMLSaveOptions` и `PdfSaveOptions`.

#### **Установите параметр экспорта для PDF.**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением в формате от diagram до PDF.

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

#### **Установите параметр экспорта для HTML.**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением в формате от diagram до HTML.

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

#### **Установите параметр экспорта для изображения**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением diagram в формате изображения.

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

#### **Установите параметр экспорта для SVG.**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением в формате от diagram до SVG.

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
