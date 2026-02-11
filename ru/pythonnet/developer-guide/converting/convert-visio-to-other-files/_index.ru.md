---
title:  Конвертировать Visio в другие форматы
linktitle:  Конвертировать Visio в другие форматы
type: docs
weight: 40
url: /ru/python-net/convert-visio-to-other-files/
description: В этом разделе показано, как Aspose.Diagram позволяет конвертировать Visio в форматы SVG,XPS,XML,XAML. Преобразование VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM в SVG,XPS,XML,0786 с помощью нескольких строк кода1.15,0786.
---
## **Экспорт в XML**
### **Экспорт Microsoft Visio Чертеж в PDF**
В примерах кода показано, как экспортировать чертеж Microsoft Visio в PDF с помощью C#.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the pdf format
diagram.save("Visio_out.pdf", SaveFileFormat.PDF)
{{< /highlight >}}


 В этой статье объясняется, как экспортировать Microsoft Visio diagram в XML с помощью[Aspose.Diagram для Python via .NET](https://products.aspose.com/diagram/python-net/) API.

- VDX определяет XML diagram.
- VTX определяет шаблон XML.
- VSX определяет шаблон XML.

 Конструкторы класса [Diagram] читают diagram, а метод Save используется для сохранения или экспорта diagram в другом формате файла. Фрагменты кода в этой статье показывают, как использовать метод Save для сохранения файла Visio в[VDX](https://docs.aspose.com/diagram/python-net/save-visio-document/), [VTX](https://docs.aspose.com/diagram/python-net/save-visio-document/) а также[VSX](https://docs.aspose.com/diagram/python-net/save-visio-document/).

На изображении ниже показан код diagram, который экспортируется в приведенных ниже фрагментах кода. Экспортированный файл отображается перед каждым фрагментом кода.

|**A Microsoft Visio diagram собирается на экспорт.**|
|:- |
|![дело:изображение_альтернативный_текст](how-to-convert-a-visio-diagram_3.png)|

### **Экспорт VSD в VDX**
VDX — это формат файла XML на основе схемы, который позволяет сохранять диаграммы в формате, который могут читать продукты, отличные от Microsoft Visio. Это удобный формат для передачи диаграмм между программными приложениями и сохранения редактируемых данных.

Чтобы экспортировать VSD diagram в VDX:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save класса Diagram, чтобы записать файл чертежа Visio в VDX.

|**Экспортированный файл VDX.**|
|:- |
|![дело:изображение_альтернативный_текст](how-to-convert-a-visio-diagram_4.png)|

### **Экспорт из VSD в VSX**
VSX — это формат XML для определения трафаретов, основных объектов, из которых строится diagram. Когда файл Visio преобразуется в VSX, экспортируются только наборы элементов.

Чтобы экспортировать VSD diagram в VSX:

- Создайте экземпляр класса Diagram.
- Вызовите метод Save класса Diagram, чтобы записать файл чертежа Visio в VSX.
### **Экспорт VSD в VTX**
TVX представляет собой XML-представление файла шаблона и хранит настройки документа.

Чтобы экспортировать VSD diagram в VTX:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save класса diagram, чтобы записать файл чертежа Visio в формате VTX.
### **Экспорт Microsoft Visio чертежа в XML**
В примерах кода показано, как экспортировать Microsoft Visio Drawing в XML с помощью C#.


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


## **Экспорт в XPS**
 В этой статье объясняется, как экспортировать Microsoft Visio diagram в XPS с помощью[Aspose.Diagram для Python via .NET](https://products.aspose.com/diagram/python-net/) API.
Используйте конструктор класса [Diagram] для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения.

Фрагменты кода в этой статье используют diagram ниже в качестве входных данных. Вы также можете использовать другие форматы diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VDX, VTX или VSX).

|**Исходный документ.**|
|:- |
|![дело:изображение_альтернативный_текст](how-to-convert-a-visio-diagram_5.png)|


Чтобы экспортировать VSD diagram в XPS:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save класса Diagram и установите XPS в качестве выходного формата.
### **Экспорт Microsoft Visio Чертеж в XPS**
В примерах кода показано, как экспортировать чертеж Microsoft Visio в XPS с помощью C#.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the xps format
diagram.save("Visio_out.xps", SaveFileFormat.XPS)
{{< /highlight >}}


## **Экспорт Diagram в SVG**
 В этой статье объясняется, как экспортировать Microsoft Visio diagram в SVG (масштабируемая векторная графика) с помощью[Aspose.Diagram для Python via .NET](https://products.aspose.com/diagram/python-net/) API.

Используйте конструктор класса [Diagram] для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения.

Чтобы экспортировать VSD diagram в SVG, выполните следующие действия:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save класса и установите SVG в качестве формата экспорта.
### **Экспорт Microsoft Visio Чертеж в SVG**
Примеры кода показывают, как экспортировать diagram в SVG с помощью C#.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the svg format
diagram.save("Visio_out.svg", SaveFileFormat.SVG)
{{< /highlight >}}


Чтобы экспортировать чертеж Visio с выбранными фигурами:

1. Создайте экземпляр класса Diagram.
1. Создайте экземпляр любого класса SaveOption, чтобы указать параметры, как описано здесь:[Укажите Visio Параметры сохранения](https://docs.aspose.com/diagram/python-net/save-visio-document/#specifying-visio-save-options)
1. Вызовите метод Save объекта класса Diagram и передайте объект класса опции сохранения в качестве параметра.
### **Преобразовать Visio Рисунок с образцом программирования выборочных фигур**
В примере кода показано, как экспортировать рисунок с выбранными фигурами Visio.


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
