---
title:  Конвертировать Visio в другие форматы
linktitle:  Конвертировать Visio в другие форматы
type: docs
weight: 40
url: /ru/python-java/convert-visio-to-other-files/
description: This topic show you how to convert Visio to SVG,XPS,XML,XAML formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to SVG,XPS,XML ,XAML с помощью нескольких строк кода.
---
**[A Microsoft Visio diagram для экспорта.](ExportToXML.vsd)**

## **Экспорт в XML**
В этой статье объясняется, как экспортировать Microsoft Visio diagram в XML, используя Aspose.Diagram для Python via Java.

- VDX определяет XML diagram.
- VTX определяет шаблон XML.
- VSX определяет шаблон XML.

Конструкторы класса Diagram считывают diagram, а метод Save используется для сохранения или экспорта diagram в другом формате файла. Фрагменты кода в этой статье показывают, как использовать метод Save для сохранения файла Visio в форматах VDX, VTX и VSX.

### **Экспорт VSD в VDX**
VDX — это формат файла XML на основе схемы, который позволяет сохранять диаграммы в формате, который могут читать продукты, отличные от Microsoft Visio. Это удобный формат для передачи диаграмм между программными приложениями и сохранения редактируемых данных.

Чтобы экспортировать VSD diagram в VDX:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save класса Diagram, чтобы записать файл чертежа Visio в VDX.

### **Экспорт из VSD в VSX**
VSX — это формат XML для определения трафаретов, основных объектов, из которых строится diagram. Когда файл Visio преобразуется в VSX, экспортируются только наборы элементов.

Чтобы экспортировать VSD diagram в VSX:

- Создайте экземпляр класса Diagram.
- Вызовите метод Save класса Diagram, чтобы записать файл чертежа Visio в VSX.

На изображении ниже показан выходной файл VSX. Обратите внимание, что трафареты, используемые в diagram, а не в самом diagram, экспортируются.

### **Экспорт VSD в VTX**
TVX представляет собой XML-представление файла шаблона и хранит настройки документа.

Чтобы экспортировать VSD diagram в VTX:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save класса diagram, чтобы записать файл чертежа Visio в формате VTX.

На изображении ниже показан выходной файл VTX.

### **Пример программирования экспорта в XML**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# 1. Exporting VSDX to VDX
# Call the diagram constructor to load diagram from a VSD file
diagram = Diagram("ExportToXML.vsd")

# Save input VSD as VDX
diagram.save("ExportToXML_Out.vdx", SaveFileFormat.VDX)

# 2. Exporting from VSD to VSX
# Call the diagram constructor to load diagram from a VSD file
        
# Save input VSD as VSX
diagram.save("ExportToXML_Out.vsx", SaveFileFormat.VSX)
        
# 3. Export VSD to VTX
# Save input VSD as VTX
diagram.save("ExportToXML_Out.vtx", SaveFileFormat.VTX)

jpype.shutdownJVM()

{{< /highlight >}}
```

## **Экспорт на XPS**
В этой статье объясняется, как экспортировать Microsoft Visio diagram в XPS, используя Aspose.Diagram для Python via Java.
Используйте конструктор класса Diagram для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения.

Фрагменты кода в этой статье используют diagram ниже в качестве входных данных. Вы также можете использовать другие форматы diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX или VSX).

Чтобы экспортировать VSD diagram в XPS:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save класса Diagram и установите XPS в качестве выходного формата.

На изображении ниже показан выходной файл XPS.

### **Экспорт в XPS Образец программы**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSD file
diagram = Diagram("ExportToXPS.vsd")

# Save as XPS
diagram.save("ExportToXPS_Out.xps", SaveFileFormat.XPS)

jpype.shutdownJVM()

{{< /highlight >}}
```

## **Экспорт Diagram в SVG**
В этой статье объясняется, как экспортировать Microsoft Visio diagram в SVG (масштабируемая векторная графика), используя Aspose.Diagram вместо Python via Java.

Используйте конструктор класса Diagram для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения.

Чтобы экспортировать VSD diagram в SVG, выполните следующие действия:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save класса и установите SVG в качестве формата экспорта.

### **Экспорт Diagram в SVG Образец программы**
Примеры кода показывают, как экспортировать diagram в SVG с помощью Java.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# call the diagram constructor to load diagram from a VSD file
diagram = Diagram("ExportToSVG.vsd")

# Save as SVG
diagram.save("ExportToSVG_Out.svg", SaveFileFormat.SVG)

jpype.shutdownJVM()

{{< /highlight >}}
```

## **Экспорт Diagram в XAML**
В этой статье объясняется, как экспортировать Microsoft Visio diagram в XAML (расширяемый язык разметки приложений), используя Aspose.Diagram для Python via Java.

Используйте конструктор класса Diagram для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения.

Чтобы экспортировать VSD diagram в XAML:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save класса и установите XAML в качестве формата экспорта.

### **Экспорт в XAML Образец программы**
В примере кода показано, как экспортировать diagram в XAML с помощью Java.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# call the diagram constructor to load diagram from a VSD file
diagram = Diagram("ExportToXAML.vsd")

# save as XAML
diagram.save("ExportToXAML_Out.xaml", SaveFileFormat.XAML)

jpype.shutdownJVM()

{{< /highlight >}}
```

## **Преобразовать Visio Рисунок с выбранными фигурами**
Используя Aspose.Diagram API, разработчики могут выбрать группу фигур для преобразования рисунка Visio в любой другой поддерживаемый формат. Класс RenderingSaveOptions предлагает член Shapes для поддержки группы фигур. Каждый класс параметров сохранения является расширенной формой класса RenderingSaveOptions.

Чтобы экспортировать чертеж Visio с выбранными фигурами:

1. Создайте экземпляр класса Diagram.
1. Создайте экземпляр любого класса SaveOption, чтобы указать настройки, как описано
1. Вызовите метод сохранения объекта класса Diagram и передайте объект класса параметра сохранения в качестве параметра.

### **Преобразовать Visio Рисунок с образцом программирования выборочных фигур**
В примере кода показано, как экспортировать рисунок с выбранными фигурами Visio.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# call the diagram constructor to load diagram from a VSD file
diagram = Diagram("DrawingSimple.vsdx")

# create an instance SVG save options class
options = SVGSaveOptions()
shapes = options.getShapes()

# get shapes by page index and shape ID, and then add in the shape collection object
shapes.add(diagram.getPages().get(0).getShapes().getShape(1))
shapes.add(diagram.getPages().get(0).getShapes().getShape(2))

# save Visio drawing
diagram.save("SelectiveShapes_out.svg", options)

jpype.shutdownJVM()

{{< /highlight >}}
```