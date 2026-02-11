---
title: Проверить авторазвертывание страницы
type: docs
weight: 10
url: /ru/net/check-page-autoexpand/
description: В этом разделе объясняется, как проверить или изменить страницу, которая автоматически расширяется в файле visio с помощью Aspose.Diagram.
---
## **Изменить размер страницы**

[Страница](http://www.aspose.com/api/net/diagram/aspose.diagram/page)объект представляет область рисования страницы переднего плана или страницы фона. Свойство Pages, предоставляемое[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Класс поддерживает набор объектов Aspose.Diagram.Page.
[PageProps](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/pageprops) объект представляет атрибуты страницы, такие как ширина, высота и масштаб страницы. Это свойство можно использовать для проверки авторазвертывания страницы.

Используйте свойство PageProps для проверки авторазвертывания страницы.
### **Пример программирования установки размера страницы**
Следующий фрагмент кода автоматически расширяет страницу проверки из файла diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");
// Get Page autoexpand
bool isAutoExpand = page.PageSheet.PageProps.DrawingResizeType.Value == DrawingResizeTypeValue.Automatically ? true : false;
//Set Page autoexpand
page.PageSheet.PageProps.DrawingResizeType.Value = DrawingResizeTypeValue.NotAutomatically;

// Save Visio
diagram.Save(dataDir + "SetAutoExpand_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

