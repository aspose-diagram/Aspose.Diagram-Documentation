---
title:  Конвертировать Visio в другие форматы
linktitle:  Конвертировать Visio в другие форматы
type: docs
weight: 40
url: /ru/net/convert-visio-to-other-files/
description: В этом разделе показано, как Aspose.Diagram позволяет конвертировать Visio в форматы SVG,XPS,XML,XAML. Преобразование VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM в SVG,XPS,XML,0786 с помощью нескольких строк кода1.15,0786.
---
## **Экспорт в XML**
### **Экспорт Microsoft Visio Чертеж в PDF**
В примерах кода показано, как экспортировать чертеж Microsoft Visio в PDF с помощью C#.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExportToPDF.vsd");

MemoryStream pdfStream = new MemoryStream();
// Save diagram
diagram.Save(pdfStream, SaveFileFormat.PDF);

// Create a PDF file
FileStream pdfFileStream = new FileStream(dataDir + "ExportToPDF_out.pdf", FileMode.Create, FileAccess.Write);
pdfStream.WriteTo(pdfFileStream);
pdfFileStream.Close();

pdfStream.Close();

// Display Status.
System.Console.WriteLine("Conversion from vsd to pdf performed successfully.");

{{< /highlight >}}
```

 В этой статье объясняется, как экспортировать Microsoft Visio diagram в XML с помощью[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

- VDX определяет XML diagram.
- VTX определяет шаблон XML.
- VSX определяет шаблон XML.

[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) конструкторы класса читают diagram, а метод Save используется для сохранения или экспорта diagram в другом формате файла. Фрагменты кода в этой статье показывают, как использовать метод Save для сохранения файла Visio в[VDX](https://docs.aspose.com/diagram/net/save-visio-document/), [VTX](https://docs.aspose.com/diagram/net/save-visio-document/) а также[VSX](https://docs.aspose.com/diagram/net/save-visio-document/).

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

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
            
/* 1. Exporting VSDX to VDX */
// Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToXML.vsd");

// Save input VSD as VDX
diagram.Save(dataDir + "ExportToXML_out.vdx", SaveFileFormat.VDX);

/* 2. Exporting from VSD to VSX */
// Call the diagram constructor to load diagram from a VSD file
            
// Save input VSD as VSX
diagram.Save(dataDir + "ExportToXML_out.vsx", SaveFileFormat.VSX);
            
/* 3. Export VSD to VTX */
// Save input VSD as VTX
diagram.Save(dataDir + "ExportToXML_out.vtx", SaveFileFormat.VTX);

{{< /highlight >}}
```

## **Экспорт в XPS**
 В этой статье объясняется, как экспортировать Microsoft Visio diagram в XPS с помощью[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.
 Использовать[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения.

Фрагменты кода в этой статье используют diagram ниже в качестве входных данных. Вы также можете использовать другие форматы diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VDX, VTX или VSX).

|**Исходный документ.**|
|:- |
|![дело:изображение_альтернативный_текст](how-to-convert-a-visio-diagram_5.png)|


Чтобы экспортировать VSD diagram в XPS:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save класса Diagram и установите XPS в качестве выходного формата.
### **Экспорт Microsoft Visio Чертеж в XPS**
В примерах кода показано, как экспортировать чертеж Microsoft Visio в XPS с помощью C#.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Open a VSD file
Diagram diagram = new Diagram(dataDir + "LayOutShapesInCompactTreeStyle.vdx");

// Save diagram to an XPS format
diagram.Save(dataDir + "ExportToXPS_out.xps", SaveFileFormat.XPS);

{{< /highlight >}}
```

## **Экспорт Diagram в SVG**
 В этой статье объясняется, как экспортировать Microsoft Visio diagram в SVG (масштабируемая векторная графика) с помощью[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

 Использовать[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения.

Чтобы экспортировать VSD diagram в SVG, выполните следующие действия:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save класса и установите SVG в качестве формата экспорта.
### **Экспорт Microsoft Visio Чертеж в SVG**
Примеры кода показывают, как экспортировать diagram в SVG с помощью C#.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExportToSVG.vsd");

// Save SVG Output file
diagram.Save(dataDir + "Output.svg", SaveFileFormat.SVG);

{{< /highlight >}}
```
## **Экспорт в SWF**
 В этой статье объясняется, как экспортировать Microsoft Visio diagram в SWF с помощью[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

 Использовать[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)конструкторы класса для чтения файлов diagram, а затем метод Save класса Diagram для экспорта формата diagram в формат SWF. The image below shows the input VSD file that the code renders to SWF. You can use other diagram formats (VSS, VSSX, VSSM, VDW, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

|**Введите diagram.**|
|:- |
|![дело:изображение_альтернативный_текст](how-to-convert-a-visio-diagram_7.png)|

После кода есть изображение вывода.

Для экспорта VSD diagram в SWF:

- Создайте экземпляр класса Diagram.
- Вызовите метод Save класса Diagram и укажите формат SWF, чтобы экспортировать diagram в SWF.
### **Пример программирования встроенного средства просмотра**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();
// Load diagram
Diagram diagram = new Diagram(dataDir + "ActvDir.vsd");
// Save diagram
diagram.Save(dataDir + "Output_out.swf", SaveFileFormat.SWF);

{{< /highlight >}}
```
### **Пример программирования без средства просмотра**
Файл SWF, созданный этими фрагментами кода, включает средство просмотра SWF. Исключите средство просмотра SWF из файла, используя следующий код.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Instantiate Diagram Object and open VSD file
Diagram diagram = new Diagram(dataDir + "ExportToSWFWithoutViewer.vsd");

// Instantiate the Save Options
SWFSaveOptions options = new SWFSaveOptions();

// Set Save format as SWF
options.SaveFormat = SaveFileFormat.SWF;

// Exclude the embedded viewer
options.ViewerIncluded = false;

// Save the resultant SWF file
diagram.Save(dataDir + "ExportToSWFWithoutViewer_out.swf", SaveFileFormat.SWF);

{{< /highlight >}}
```
## **Экспорт Diagram в XAML**
В этой статье объясняется, как экспортировать Microsoft Visio diagram в XAML (расширяемый язык разметки приложений) с помощью[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

 Использовать[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения.

Чтобы экспортировать VSD diagram в XAML:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save класса и установите XAML в качестве формата экспорта.
### **Экспорт Microsoft Visio Чертеж в XAML**
В примере кода показано, как экспортировать diagram в XAML с помощью C#.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
// Load diagram
Diagram diagram = new Diagram(dataDir + "ExportToXAML.vsd");
// Save diagram
diagram.Save(dataDir + "ExportToXAML_out.xaml", SaveFileFormat.XAML);

{{< /highlight >}}
```
## **Преобразовать Visio Рисунок с выбранными фигурами**
Используя Aspose.Diagram API, разработчики могут выбрать группу фигур для преобразования рисунка Visio в любой другой поддерживаемый формат. Класс RenderingSaveOptions предлагает член Shapes для поддержки группы фигур. Каждый класс параметров сохранения является расширенной формой класса RenderingSaveOptions.

Чтобы экспортировать чертеж Visio с выбранными фигурами:

1. Создайте экземпляр класса Diagram.
1. Создайте экземпляр любого класса SaveOption, чтобы указать параметры, как описано здесь:[Укажите Visio Параметры сохранения](https://docs.aspose.com/diagram/net/save-visio-document/#specifying-visio-save-options)
1. Вызовите метод Save объекта класса Diagram и передайте объект класса опции сохранения в качестве параметра.
### **Преобразовать Visio Рисунок с образцом программирования выборочных фигур**
В примере кода показано, как экспортировать рисунок с выбранными фигурами Visio.

```
{{< highlight "csharp" >}}
// the path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance SVG save options class
SVGSaveOptions options = new SVGSaveOptions();
ShapeCollection shapes = options.Shapes;

// get shapes by page index and shape ID, and then add in the shape collection object
shapes.Add(diagram.Pages[0].Shapes.GetShape(1));
shapes.Add(diagram.Pages[0].Shapes.GetShape(2));

// save Visio drawing
diagram.Save(dataDir + "SelectiveShapes_out.svg", options);
{{< /highlight >}}
```