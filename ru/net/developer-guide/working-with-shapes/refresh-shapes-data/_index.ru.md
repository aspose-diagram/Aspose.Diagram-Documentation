---
title: Обновить данные фигур
type: docs
weight: 40
url: /ru/net/refresh-shapes-data/
description: В этом разделе объясняется, как обновить данные фигуры для фигуры visio с помощью Aspose.Diagram.
---
## **Обновляет положение фигуры, включая xform, соединение и геометрию при изменении текста формы или других**
 Метод RefreshData, предоставляемый[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) класс может использоваться для обновления данных фигуры

В приведенном ниже коде показано, как:

1. Загрузите образец файла.
1. Доступ к определенной форме.
1. Обновить данные фигуры.
### **Обновить данные Shape**
Используйте следующий код в своем приложении .NET, чтобы обновить фигуру с помощью Aspose.Diagram for .NET.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

// Get Shape
Shape shape = page.Shapes.GetShape(15);

// Refresh data
shape.RefreshData();

// Save visio diagram
diagram.Save(dataDir + "RefreshData_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

