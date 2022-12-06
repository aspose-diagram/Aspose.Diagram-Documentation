---
title: Общедоступный API Изменения в Aspose.Diagram 6.3.0
type: docs
weight: 40
url: /ru/java/public-api-changes-in-aspose-diagram-6-3-0/
---
{{% alert color="primary" %}} 

В этом документе описаны изменения в Aspose.Diagram API с версии 6.0.0 до 6.3.0, которые могут представлять интерес для разработчиков модулей/приложений. Он включает в себя не только новые и обновленные общедоступные методы, но и описание любых изменений в поведении за кулисами в Aspose.Diagram.

{{% /alert %}} 
## **Определить формат файла Visio**
### **Добавлены различные классы, методы и свойства для определения формата**
- **Добавьте классы FileFormatUtil и FileFormatInfo.** 
 - Эти классы предоставляют программный доступ для определения типа файла Visio.
- **Добавляет метод detectFileFormat в класс FileFormatUtil.** 
 - Он обнаруживает и возвращает информацию о формате сохраненного Visio diagram в файле.
- **Добавляет свойство FileFormatType в класс FileFormatInfo** 
 - Он получает обнаруженный формат файла.
- **Добавляет свойство LoadFormat в FileFormatInfo** 
 - Он получает обнаруженный формат загрузки.

 Разработчики могут легко определить формат любого файла Visio. В этом разделе справки показано, как определить формат файла Visio (используя путь к файлу или поток) и проверить его расширение:[Определить формат файла Visio](/diagram/ru/java/introduction/#Introduction-DetecttheFormatofVisioFile)
## **Управление экспортом скрытых Visio страниц при сохранении**
### **Добавляет setExportHiddenPage в классы SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions и PdfSaveOptions.**
- Он определяет, нужно ли экспортировать скрытые страницы Visio или нет.

 Разработчики могут включать или исключать скрытые страницы Visio при сохранении Visio diagram в файлы PDF, HTML, изображения (PNG, JPEG, GIF), SVG и XPS. В этом разделе справки показано, как это сделать:[Управление экспортом скрытых Visio страниц при сохранении](/diagram/ru/java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/#control-the-export-of-hidden-visio-pages-on-saving)
