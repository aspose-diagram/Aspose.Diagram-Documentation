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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-SetVisioPageOrientation-SetVisioPageOrientation.cs" >}}
## **Управление экспортом скрытых Visio страниц при сохранении**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)API позволяет разработчикам включать или исключать Visio скрытые страницы при сохранении файлов с diagram по PDF, HTML, изображений (PNG, JPEG, GIF), SVG и XPS. Даже они могут скрыть страницы Aspose.Diagram, используя Aspose.Diagram API, потому что эта опция уже доступна через ячейку UIVisibility в ShapeSheet страницы.
### **Скрыть страницу в Visio Diagram и установить параметр экспорта**
 Aspose.Diagram for .NET API имеет[Страница](http://www.aspose.com/api/net/diagram/aspose.diagram/page) класс, представляющий страницу рисования Visio. Свойство PageSheet, предоставляемое классом Page, также предоставляет свойства страницы. Поле UIVisibility свойств страницы позволяет скрыть страницу. Затем разработчики могут использовать свойство ExportHiddenPage, которое добавляется в классы SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions и PdfSaveOptions.
#### **Установите параметр экспорта для PDF.**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением в формате от diagram до PDF.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToPDF-ExportOfHiddenVisioPagesToPDF.cs" >}}
#### **Установите параметр экспорта для HTML.**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением в формате от diagram до HTML.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToHTML-ExportOfHiddenVisioPagesToHTML.cs" >}}
#### **Установите параметр экспорта для изображения**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением diagram в формате изображения.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToImage-ExportOfHiddenVisioPagesToImage.cs" >}}
#### **Установите параметр экспорта для SVG.**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением в формате от diagram до SVG.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToSVG-ExportOfHiddenVisioPagesToSVG.cs" >}}
#### **Установите параметр экспорта для XPS.**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением в формате от diagram до XPS.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToXPS-ExportOfHiddenVisioPagesToXPS.cs" >}}
