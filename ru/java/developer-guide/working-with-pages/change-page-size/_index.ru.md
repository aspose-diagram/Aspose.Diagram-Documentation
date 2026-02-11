---
title: Изменить размер страницы
type: docs
weight: 10
url: /ru/java/change-page-size/
description: В этом разделе объясняется, как изменить размер страницы в файле visio на Aspose.Diagram.
---
## **Изменить размер страницы**

[Страница](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)объект представляет область рисования страницы переднего плана или страницы фона. Свойство Pages, предоставляемое[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) Класс поддерживает набор объектов Aspose.Diagram.Page.
[PageProps](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageProps) объект представляет атрибуты страницы, такие как ширина, высота и масштаб страницы. Это свойство можно использовать для изменения размера страницы.

Используйте свойство PageProps для изменения размера страницы.
### **Пример программирования установки размера страницы**
Следующий фрагмент кода изменяет размер страницы с diagram.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ChangeVisioPageSize.class);
      
// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Page page = diagram.getPages().getPage("Flow 1");
// Set Page Size
page.getPageSheet().getPageProps().getPageHeight().setValue(8);
page.getPageSheet().getPageProps().getPageWidth().setValue(11);

// Save Visio
diagram.save(dataDir + "SetPageSize_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

