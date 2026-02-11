---
title: Проверить авторазвертывание страницы
type: docs
weight: 10
url: /ru/java/check-page-autoexpand/
description: В этом разделе объясняется, как проверить или изменить страницу, которая автоматически расширяется в файле visio с помощью Aspose.Diagram.
---
## **Проверить авторазвертывание страницы**

[Страница](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)объект представляет область рисования страницы переднего плана или страницы фона. Свойство Pages, предоставляемое[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) Класс поддерживает набор объектов Aspose.Diagram.Page.
[PageProps](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageProps) объект представляет атрибуты страницы, такие как ширина, высота и масштаб страницы. Это свойство можно использовать для проверки авторазвертывания страницы.

Используйте свойство PageProps для проверки авторазвертывания страницы.
### **Пример программирования автоматического расширения страницы проверки**
Следующий фрагмент кода автоматически расширяет страницу проверки из файла diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CheckChangeAutoExpand.class);
      
// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Page page = diagram.getPages().getPage("Page-2");
// Get Page autoexpand
boolean isAutoExpand = page.getPageSheet().getPageProps().getDrawingResizeType().getValue() == DrawingResizeTypeValue.AUTOMATICALLY ? true : false;
//Set Page autoexpand
page.getPageSheet().getPageProps().getDrawingResizeType().setValue(DrawingResizeTypeValue.NOT_AUTOMATICALLY);

// Save Visio
diagram.save(dataDir + "SetAutoExpand_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
