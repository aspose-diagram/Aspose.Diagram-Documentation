---
title:  Конвертировать Visio в другие форматы
linktitle:  Конвертировать Visio в другие форматы
type: docs
weight: 40
url: /ru/java/convert-visio-to-other-files/
description: В этом разделе показано, как Aspose.Diagram позволяет конвертировать Visio в форматы SVG,XPS,XML,XAML. Преобразование VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM в SVG,XPS,XML,0786 с помощью нескольких строк кода1.15,0786.
---
## **Экспорт в XML**
 В этой статье объясняется, как экспортировать Microsoft Visio diagram в XML с помощью[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

- VDX определяет XML diagram.
- VTX определяет шаблон XML.
- VSX определяет шаблон XML.

[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) конструкторы класса читают diagram, а метод Save используется для сохранения или экспорта diagram в другом формате файла. Фрагменты кода в этой статье показывают, как использовать метод Save для сохранения файла Visio в[VDX](/diagram/ru/java/how-to-convert-a-visio-diagram/), [VTX](/diagram/ru/java/how-to-convert-a-visio-diagram/) а также[VSX](/diagram/ru/java/how-to-convert-a-visio-diagram/).

На изображении ниже показан код diagram, который экспортируется в приведенных ниже фрагментах кода. Экспортированный файл отображается перед каждым фрагментом кода.

**A Microsoft Visio diagram собирается на экспорт.**

![дело:изображение_альтернативный_текст](http://i.imgur.com/XWajazh.png)
### **Экспорт VSD в VDX**
VDX — это формат файла XML на основе схемы, который позволяет сохранять диаграммы в формате, который могут читать продукты, отличные от Microsoft Visio. Это удобный формат для передачи диаграмм между программными приложениями и сохранения редактируемых данных.

Чтобы экспортировать VSD diagram в VDX:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save класса Diagram, чтобы записать файл чертежа Visio в VDX.

**Экспортированный файл VDX.**

![дело:изображение_альтернативный_текст](http://i.imgur.com/OJ1jpgh.png)
### **Экспорт из VSD в VSX**
VSX — это формат XML для определения трафаретов, основных объектов, из которых строится diagram. Когда файл Visio преобразуется в VSX, экспортируются только наборы элементов.

Чтобы экспортировать VSD diagram в VSX:

- Создайте экземпляр класса Diagram.
- Вызовите метод Save класса Diagram, чтобы записать файл чертежа Visio в VSX.

На изображении ниже показан выходной файл VSX. Обратите внимание, что трафареты, используемые в diagram, а не в самом diagram, экспортируются.

**Экспортированный файл VSX.**

![дело:изображение_альтернативный_текст](http://i.imgur.com/gkZrxCN.png)
### **Экспорт VSD в VTX**
TVX представляет собой XML-представление файла шаблона и хранит настройки документа.

Чтобы экспортировать VSD diagram в VTX:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save класса diagram, чтобы записать файл чертежа Visio в формате VTX.

На изображении ниже показан выходной файл VTX.

**Выходной файл VTX.**

![дело:изображение_альтернативный_текст](http://i.imgur.com/E6pUvGD.jpg)
### **Пример программирования экспорта в XML**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToXML-ExportToXML.java" >}}
## **Экспорт на XPS**
 В этой статье объясняется, как экспортировать Microsoft Visio diagram в XPS с помощью[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.
 Использовать[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class' для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения.

Фрагменты кода в этой статье используют diagram ниже в качестве входных данных. Вы также можете использовать другие форматы diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX или VSX).

**Исходный документ.**

![дело:изображение_альтернативный_текст](http://i.imgur.com/P3gaA34.png)

Чтобы экспортировать VSD diagram в XPS:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save класса Diagram и установите XPS в качестве выходного формата.

На изображении ниже показан выходной файл XPS.

**Вывод XPS.**

![дело:изображение_альтернативный_текст](http://i.imgur.com/1ESRxSy.png)
### **Экспорт в XPS Образец программы**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToXPS-ExportToXPS.java" >}}
## **Экспорт Diagram в SVG**
 В этой статье объясняется, как экспортировать Microsoft Visio diagram в SVG (масштабируемая векторная графика) с помощью[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Использовать[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class' для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения.

Чтобы экспортировать VSD diagram в SVG, выполните следующие действия:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save класса и установите SVG в качестве формата экспорта.
### **Экспорт Diagram в SVG Образец программы**
Примеры кода показывают, как экспортировать diagram в SVG с помощью Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToSVG-ExportToSVG.java" >}}
## **Экспорт Diagram в XAML**
В этой статье объясняется, как экспортировать Microsoft Visio diagram в XAML (расширяемый язык разметки приложений) с помощью[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Использовать[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class' для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения.

Чтобы экспортировать VSD diagram в XAML:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save класса и установите XAML в качестве формата экспорта.
### **Экспорт в XAML Образец программы**
В примере кода показано, как экспортировать diagram в XAML с помощью Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToXAML-ExportToXAML.java" >}}

## **Преобразовать Visio Рисунок с выбранными фигурами**
Используя Aspose.Diagram API, разработчики могут выбрать группу фигур для преобразования рисунка Visio в любой другой поддерживаемый формат. Класс RenderingSaveOptions предлагает член Shapes для поддержки группы фигур. Каждый класс параметров сохранения является расширенной формой класса RenderingSaveOptions.

Чтобы экспортировать чертеж Visio с выбранными фигурами:

1. Создайте экземпляр класса Diagram.
1. Создайте экземпляр любого класса SaveOption, чтобы указать параметры, как описано здесь:[Укажите Visio Параметры сохранения](https://docs.aspose.com/diagram/java/save-a-visio-drawing-to-pdf-html-and-other-formats/#specifying-visio-save-options)
1. Вызовите метод сохранения объекта класса Diagram и передайте объект класса параметра сохранения в качестве параметра.
### **Преобразовать Visio Рисунок с образцом программирования выборочных фигур**
В примере кода показано, как экспортировать рисунок с выбранными фигурами Visio.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ConvertVisioWithSelectiveShapes.Java" >}}