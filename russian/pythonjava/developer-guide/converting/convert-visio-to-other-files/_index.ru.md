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
В этой статье объясняется, как экспортировать Microsoft Visio diagram в XML, используя Aspose.Diagram для Python через Java.

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
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToXML.py" >}}

## **Экспорт в XPS**
В этой статье объясняется, как экспортировать Microsoft Visio diagram в XPS, используя Aspose.Diagram для Python через Java.
Используйте конструктор класса Diagram для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения.

Фрагменты кода в этой статье используют diagram ниже в качестве входных данных. Вы также можете использовать другие форматы diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX или VSX).

Чтобы экспортировать VSD diagram в XPS:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save класса Diagram и установите XPS в качестве выходного формата.

На изображении ниже показан выходной XPS-файл.

### **Пример программирования экспорта в XPS**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToXPS.py" >}}

## **Экспорт Diagram в SVG**
В этой статье объясняется, как экспортировать Microsoft Visio diagram в SVG (масштабируемую векторную графику), используя Aspose.Diagram вместо Python через Java.

Используйте конструктор класса Diagram для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения.

Чтобы экспортировать VSD diagram в SVG, выполните следующие действия:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save класса и установите SVG в качестве формата экспорта.

### **Экспорт Diagram в пример программирования SVG**
Примеры кода показывают, как экспортировать diagram в SVG, используя Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToSVG.py" >}}

## **Экспорт Diagram в XAML**
В этой статье объясняется, как экспортировать Microsoft Visio diagram в XAML (расширяемый язык разметки приложений), используя Aspose.Diagram для Python через Java.

Используйте конструктор класса Diagram для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения.

Чтобы экспортировать VSD diagram в XAML:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save класса и установите XAML в качестве формата экспорта.

### **Пример программирования экспорта в XAML**
В примере кода показано, как экспортировать diagram в XAML с помощью Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToXAML.py" >}}

## **Преобразовать Visio Рисунок с выбранными фигурами**
Используя Aspose.Diagram API, разработчики могут выбрать группу фигур для преобразования рисунка Visio в любой другой поддерживаемый формат. Класс RenderingSaveOptions предлагает член Shapes для поддержки группы фигур. Каждый класс параметров сохранения является расширенной формой класса RenderingSaveOptions.

Чтобы экспортировать чертеж Visio с выбранными фигурами:

1. Создайте экземпляр класса Diagram.
1. Создайте экземпляр любого класса SaveOption, чтобы указать настройки, как описано
1. Вызовите метод сохранения объекта класса Diagram и передайте объект класса параметра сохранения в качестве параметра.

### **Преобразовать Visio Рисунок с образцом программирования выборочных фигур**
В примере кода показано, как экспортировать рисунок с выбранными фигурами Visio.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ConvertVisioWithSelectiveShapes.py" >}}