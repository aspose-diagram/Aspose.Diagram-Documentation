---
title: Сохранить документ Visio программно
linktitle: Сохранить документ Visio
type: docs
weight: 30
url: /ru/python-net/save-visio-document/
description: На этой странице описывается, как сохранить документ Visio в файл, поток с библиотекой Aspose.Diagram.
---
## **Visio Обзор сохранения чертежа**
 Использовать[Diagram.Save]() метод сохранения чертежа Microsoft Visio. Есть перегрузки, позволяющие сохранить рисунок в файл. Чертеж можно сохранить в любом формате сохранения, поддерживаемом Aspose.Diagram. Список всех поддерживаемых форматов сохранения см.[СохранитьФайлФормат]() перечисление.
## **Сохранение Visio Diagram**
 Класс Diagram класса Aspose.Diagram API представляет чертеж Visio, и разработчики могут сохранять его объект Visio diagram в любом поддерживаемом формате файла. Чтобы сохранить файл Microsoft Visio, просто используйте[Diagram.Save]()метод, он принимает имя файла с полным путем или объект файлового потока. Aspose.Diagram API выводит формат сохранения из расширения файла, а также предлагает дополнительный параметр SaveFileFormat для указания формата выходного файла.
### **Сохраните Visio Diagram в любом поддерживаемом формате файла**
Используя Aspose.Diagram API, разработчики могут сохранить Visio diagram в любом поддерживаемом формате файла, как указано ниже:
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG, SWF and XAML**
### **Сохранение Diagram Пример программирования**
В приведенном ниже примере документ сохраняется в файл.

{{< highlight "java" >}}

 // Save a Visio diagram

diagram.Save(GetMyDir() + "MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Указание Visio параметров сохранения**
 Есть несколько[Diagram.Save]()перегрузки методов, которые принимают объект SaveOptions. Это должен быть объект класса, производного от класса SaveOptions. У каждого формата сохранения есть соответствующий класс, который содержит параметры сохранения для этого формата сохранения. Например, есть PdfSaveOptions для формата сохранения SaveFileFormat.PDF.
### **Visio Diagram Параметры сохранения**
Эти примеры показывают, как:

- [Используйте параметры сохранения Diagram](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Используйте параметры сохранения PDF](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Используйте параметры сохранения HTML](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Используйте параметры сохранения изображения](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Используйте параметры сохранения SVG](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Используйте параметры сохранения SWF](https://docs.aspose.com/diagram/python-net/save-visio-document/).
#### **Использование параметров сохранения Diagram**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением документа в формате Visio.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

options = saving.DiagramSaveOptions(SaveFileFormat.VSDX)

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", options)
{{< /highlight >}}




#### **Использование параметров сохранения PDF**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением документа в формате PDF.


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




#### **Использование параметров сохранения HTML**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением документа в формате файла HTML.


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




#### **Использование параметров сохранения изображения**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением документа в формате файла изображения.




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



Использование параметров сохранения SVG

В приведенном ниже коде показано, как установить параметры сохранения перед сохранением документа в формате SVG.


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


Иногда разработчикам необходимо программно сохранять или экспортировать диаграммы Visio в различные форматы файлов (например, VDX, PDF, JPEG и т. д.).

### ` `**Сохранение файла VSD в другие форматы с помощью Aspose.Diagram для Python via .NET**
Используя Aspose.Diagram, разработчикам не нужно Microsoft Office Visio в машине, и они могут работать независимо от Microsoft Office Автоматизация.

Фрагменты кода ниже показывают, как:

1. Загрузите diagram.
1. Сохраните diagram в VSX, PDF и JPEG.
#### **Сохранение файла VSD с Aspose.Diagram для Python via .NET Пример программирования**
{{% alert color="primary" %}} 

импорт aspose.diagram
из aspose.diagram импорт *

{{% /alert %}} 

**Пример:**


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

