---
title: Установка ориентации и управление экспортом скрытых Visio страниц при сохранении
type: docs
weight: 20
url: /ru/java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
---
## **Измените макет страницы Visio на книжный или альбомный**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API позволяет разработчикам программно устанавливать ориентацию страницы чертежа Visio. В этом разделе справки объясняется, как выполнить эту задачу.

 Aspose.Diagram for Java API имеет[Страница](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) класс, представляющий страницу рисования Visio. Свойство PageSheet, предоставляемое классом Page, также предоставляет свойства печати. Поле PrintPageOrientation свойств печати позволяет поворачивать страницу. Он предлагает три варианта: портретный, альбомный и такой же, как на принтере. Поле PrintPageOrientation можно задать программно, используя Aspose.Diagram API.

Этот пример работает следующим образом:

1. Загрузите существующий Visio diagram в объект класса Diagram.
1. Извлечь страницу Visio
1. Установите его ориентацию как Книжная, Альбомная или такая же, как на принтере.
1. Сохраните номер Visio diagram.
### **Пример программирования установки ориентации**
В приведенном ниже примере кода показано, как установить ориентацию страницы Visio.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetVisioPageOrientation.class);  
// initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get Visio page
Page page = diagram.getPages().getPage("Flow 1");
// page orientation
page.getPageSheet().getPrintProps().getPrintPageOrientation().setValue(PrintPageOrientationValue.LANDSCAPE);
// save Visio
diagram.save(dataDir + "SetPageOrientation_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Управление экспортом скрытых Visio страниц при сохранении**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API позволяет разработчикам включать или исключать Visio скрытые страницы при сохранении файлов с diagram по PDF, HTML, изображений (PNG, JPEG, GIF), SVG и XPS. Даже они могут скрыть страницы Aspose.Diagram, используя Aspose.Diagram API, потому что эта опция уже доступна через ячейку UIVisibility в ShapeSheet страницы.
### **Скрыть страницу в Visio Diagram и установить параметр экспорта**
 Aspose.Diagram for Java API имеет[Страница](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) класс, представляющий страницу рисования Visio. Свойство PageSheet, предоставляемое классом Page, также предоставляет свойства страницы. Поле UIVisibility свойств страницы позволяет скрыть страницу. Затем разработчики могут использовать свойство ExportHiddenPage, которое добавляется в классы SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions и PdfSaveOptions.
#### **Установите параметр экспорта для PDF.**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением в формате от diagram до PDF.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExporToHiddenVisioPagesToPdf.class);  
        
// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Flow 2");
// set Visio page visiblity
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE);

// initialize PDF save options
PdfSaveOptions options = new PdfSaveOptions();
// set export option of hidden Visio pages
options.setExportHiddenPage(false);

//Save the Visio diagram
diagram.save(dataDir + "ExportOfHiddenVisioPagesToPDF_Out.pdf", options);

{{< /highlight >}}
```
#### **Установите параметр экспорта для HTML.**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением в формате от diagram до HTML.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(ExportOfHiddenVisioPagesToHtml.class) + "Pages/";

// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Flow 2");
// set Visio page visiblity
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE);

// initialize PDF save options
HTMLSaveOptions options = new HTMLSaveOptions();
// set export option of hidden Visio pages
options.setExportHiddenPage(false);
// set export option of comments
options.setExportComments(false);
// Save the Visio diagram
diagram.save(dataDir + "ExportOfHiddenVisioPagesToHTML_Out.html", options);

{{< /highlight >}}
```
#### **Установите параметр экспорта для изображения**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением diagram в формате изображения.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(ExportOfHiddenVisioPagesToImage.class) + "Pages/";

// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Flow 2");
// set Visio page visiblity
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE);
// initialize PDF save options
ImageSaveOptions options = new ImageSaveOptions(SaveFileFormat.JPEG);
// set export option of hidden Visio pages
options.setExportHiddenPage(false);
// set export option of comments
options.setExportComments(false);

// Save the Visio diagram
diagram.save(dataDir + "ExportOfHiddenVisioPagesToImage_Out.jpeg", options);

{{< /highlight >}}
```
#### **Установите параметр экспорта для SVG.**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением в формате от diagram до SVG.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(ExportOfHiddenVisioPagesToSVG.class) + "Pages/";

// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Flow 2");
// set Visio page visiblity
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE);

// initialize PDF save options
SVGSaveOptions options = new SVGSaveOptions();
// set export option of hidden Visio pages
options.setExportHiddenPage(false);
// Set SVG fit to view port
options.setSVGFitToViewPort(true);
// Set export element as Rectangle
options.setExportElementAsRectTag(true);

// save the Visio diagram
diagram.save(dataDir + "ExportOfHiddenVisioPagesToSVG_Out.svg", options);

{{< /highlight >}}
```
