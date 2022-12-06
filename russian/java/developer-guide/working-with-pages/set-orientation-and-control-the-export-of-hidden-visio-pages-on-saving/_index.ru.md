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

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-SetVisioPageOrientation-SetVisioPageOrientation.java" >}}
## **Управление экспортом скрытых Visio страниц при сохранении**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API позволяет разработчикам включать или исключать Visio скрытые страницы при сохранении diagram в файлы PDF, HTML, изображения (PNG, JPEG, GIF), SVG и XPS. Даже они могут скрыть страницы Visio, используя Aspose.Diagram API, потому что эта опция уже доступна через ячейку UIVisibility на странице ShapeSheet.
### **Скрыть страницу в Visio Diagram и установить параметр экспорта**
 Aspose.Diagram for Java API имеет[Страница](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) класс, представляющий страницу рисования Visio. Свойство PageSheet, предоставляемое классом Page, также предоставляет свойства страницы. Поле UIVisibility свойств страницы позволяет скрыть страницу. Затем разработчики могут использовать свойство ExportHiddenPage, которое добавляется в классы SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions и PdfSaveOptions.
#### **Установите параметр экспорта для PDF**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением diagram в формате PDF.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExporToHiddenVisioPagesToPdf-ExporToHiddenVisioPagesToPdf.java" >}}
#### **Установите параметр экспорта для HTML**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением diagram в формате HTML.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExportOfHiddenVisioPagesToHtml-ExportOfHiddenVisioPagesToHtml.java" >}}
#### **Установите параметр экспорта для изображения**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением diagram в формате изображения.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExportOfHiddenVisioPagesToImage-ExportOfHiddenVisioPagesToImage.java" >}}
#### **Установите параметр экспорта для SVG**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением diagram в формате SVG.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExportOfHiddenVisioPagesToSVG-ExportOfHiddenVisioPagesToSVG.java" >}}
