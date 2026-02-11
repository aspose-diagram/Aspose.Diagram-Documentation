---
title: Установка ориентации и управление экспортом скрытых Visio страниц при сохранении
type: docs
weight: 20
url: /ru/net/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
description: В этом разделе объясняется, как настроить макет страницы с помощью Aspose.Diagram.
---
## **Измените макет страницы Visio на книжный или альбомный**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API позволяет разработчикам программно устанавливать ориентацию страницы чертежа Visio. В этом разделе справки объясняется, как выполнить эту задачу.

 Aspose.Diagram for .NET API имеет[Страница](http://www.aspose.com/api/net/diagram/aspose.diagram/page) класс, представляющий страницу рисования Visio. Свойство PageSheet, предоставляемое классом Page, также предоставляет свойства печати. Поле PrintPageOrientation свойств печати позволяет поворачивать страницу. Он предлагает три варианта: портретный, альбомный и такой же, как на принтере. Поле PrintPageOrientation можно задать программно, используя Aspose.Diagram API.

Этот пример работает следующим образом:

1. Загрузите существующий Visio diagram в объект класса Diagram.
1. Извлечь страницу Visio
1. Установите его ориентацию как Книжная, Альбомная или такая же, как на принтере.
1. Сохраните номер Visio diagram.
### **Пример программирования установки ориентации**
В приведенном ниже примере кода показано, как установить ориентацию страницы Visio.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");
// Page orientation
page.PageSheet.PrintProps.PrintPageOrientation.Value = PrintPageOrientationValue.Landscape;
// Save Visio
diagram.Save(dataDir + "SetPageOrientation_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Управление экспортом скрытых Visio страниц при сохранении**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)API позволяет разработчикам включать или исключать Visio скрытые страницы при сохранении файлов с diagram по PDF, HTML, изображений (PNG, JPEG, GIF), SVG и XPS. Даже они могут скрыть страницы Aspose.Diagram, используя Aspose.Diagram API, потому что эта опция уже доступна через ячейку UIVisibility в ShapeSheet страницы.
### **Скрыть страницу в Visio Diagram и установить параметр экспорта**
 Aspose.Diagram for .NET API имеет[Страница](http://www.aspose.com/api/net/diagram/aspose.diagram/page) класс, представляющий страницу рисования Visio. Свойство PageSheet, предоставляемое классом Page, также предоставляет свойства страницы. Поле UIVisibility свойств страницы позволяет скрыть страницу. Затем разработчики могут использовать свойство ExportHiddenPage, которое добавляется в классы SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions и PdfSaveOptions.
#### **Установите параметр экспорта для PDF.**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением в формате от diagram до PDF.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = BOOL.True;

// Initialize PDF save options
PdfSaveOptions options = new PdfSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;

// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToPDF_out.pdf", options);

{{< /highlight >}}
```
#### **Установите параметр экспорта для HTML.**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением в формате от diagram до HTML.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = UIVisibilityValue.Visible;

// Initialize PDF save options
HTMLSaveOptions options = new HTMLSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;
// Set export option of comments
options.IsExportComments = false;

// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToHTML_out.html", options);

{{< /highlight >}}
```
#### **Установите параметр экспорта для изображения**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением diagram в формате изображения.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = UIVisibilityValue.Visible;

// Initialize PDF save options
ImageSaveOptions options = new ImageSaveOptions(SaveFileFormat.JPEG);
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;
// Set export option of comments
options.IsExportComments = false;

// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToImage_out.jpeg", options);

{{< /highlight >}}
```
#### **Установите параметр экспорта для SVG.**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением в формате от diagram до SVG.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = UIVisibilityValue.Visible;

// Initialize PDF save options
SVGSaveOptions options = new SVGSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;
// Set export guide shapes 
options.ExportGuideShapes = false;
// Set save format
options.SaveFormat = Aspose.Diagram.SaveFileFormat.SVG;
// Set SVG fit to view port
options.SVGFitToViewPort = true;
// Set export element as Rectangle
options.ExportElementAsRectTag = true;


// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToSVG_out.svg", options);

{{< /highlight >}}
```
#### **Установите параметр экспорта для XPS.**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением в формате от diagram до XPS.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = BOOL.True;

// Initialize PDF save options
XPSSaveOptions options = new XPSSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;

// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToXPS_out.xps", options);

{{< /highlight >}}
```
