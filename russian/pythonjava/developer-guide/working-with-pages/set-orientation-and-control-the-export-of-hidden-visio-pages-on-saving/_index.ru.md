---
title: Установка ориентации и управление экспортом скрытых Visio страниц при сохранении
type: docs
weight: 20
url: /ru/python-java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
---
## **Измените макет страницы Visio на книжный или альбомный**
Aspose.Diagram для Python через Java API позволяет разработчикам программно устанавливать ориентацию страницы чертежа Visio. В этом разделе справки объясняется, как выполнить эту задачу.

Aspose.Diagram для Python через Java API имеет класс `Page`, который представляет страницу чертежа Visio. Свойство PageSheet, предоставляемое классом Page, также предоставляет свойства печати. Поле `PrintPageOrientation` свойств печати позволяет поворачивать страницу. Он предлагает три варианта: портретный, альбомный и такой же, как на принтере. Поле PrintPageOrientation можно установить программно, используя Aspose.Diagram для Python через Java API.

Этот пример работает следующим образом:

1. Загрузите существующий Visio diagram в объект класса Diagram.
1. Извлечь страницу Visio
1. Установите его ориентацию как Книжная, Альбомная или такая же, как на принтере.
1. Сохраните номер Visio diagram.

### **Пример программирования установки ориентации**
В приведенном ниже примере кода показано, как установить ориентацию страницы Visio.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-SetVisioPageOrientation.py" >}}

## **Управление экспортом скрытых Visio страниц при сохранении**
Aspose.Diagram для Python через Java API позволяет разработчикам включать или исключать скрытые Visio страницы при сохранении diagram в файлы PDF, HTML, изображения (PNG, JPEG, GIF), SVG и XPS. Даже они могут скрыть страницы Visio, используя Aspose.Diagram для Python через Java API, потому что эта опция уже доступна через ячейку UIVisibility в ShapeSheet страницы.

### **Скрыть страницу в Visio Diagram и установить параметр экспорта**
Aspose.Diagram для Python через Java API имеет класс `Page`, который представляет страницу чертежа Visio. Свойство PageSheet, предоставляемое классом Page, также предоставляет свойства страницы. Поле `UIVisibility` в свойствах страницы позволяет скрыть страницу. Затем разработчики могут использовать свойство `exportHiddenPage`, которое добавляется в классы `SVGSaveOptions`, `XPSSaveOptions`, `ImageSaveOptions`, `HTMLSaveOptions` и `PdfSaveOptions`.

#### **Установите параметр экспорта для PDF**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением diagram в формате PDF.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-ExporToHiddenVisioPagesToPdf.py" >}}

#### **Установите параметр экспорта для HTML**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением diagram в формате HTML.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-ExportOfHiddenVisioPagesToHtml.py" >}}

#### **Установите параметр экспорта для изображения**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением diagram в формате изображения.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-ExportOfHiddenVisioPagesToImage.py" >}}

#### **Установите параметр экспорта для SVG**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением diagram в формате SVG.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-ExportOfHiddenVisioPagesToSVG.py" >}}
