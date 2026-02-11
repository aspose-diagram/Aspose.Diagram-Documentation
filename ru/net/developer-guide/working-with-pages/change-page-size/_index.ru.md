---
title: Изменить размер страницы
type: docs
weight: 10
url: /ru/net/change-page-size/
description: В этом разделе объясняется, как изменить размер страницы в файле visio на Aspose.Diagram.
---
## **Изменить размер страницы**

[Страница](http://www.aspose.com/api/net/diagram/aspose.diagram/page)объект представляет область рисования страницы переднего плана или страницы фона. Свойство Pages, предоставляемое[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Класс поддерживает набор объектов Aspose.Diagram.Page.
[PageProps](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/pageprops) объект представляет атрибуты страницы, такие как ширина, высота и масштаб страницы. Это свойство можно использовать для изменения размера страницы.

Используйте свойство PageProps для изменения размера страницы.
### **Пример программирования установки размера страницы**
Следующий фрагмент кода изменяет размер страницы с diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");
// Set Page Size
page.PageSheet.PageProps.PageHeight.Value = 8;
page.PageSheet.PageProps.PageWidth.Value = 11;

// Save Visio
diagram.Save(dataDir + "SetPageSize_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
