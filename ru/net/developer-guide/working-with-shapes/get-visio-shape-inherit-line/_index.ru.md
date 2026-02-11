---
title: Получить Visio Строку наследования формы
type: docs
weight: 100
url: /ru/net/get-visio-shape-inherit-line/
description: В этом разделе объясняется, как получить стиль линии фигуры visio, унаследованный от его родительского стиля, и мастер с Aspose.Diagram.
---
### **Получить унаследованные данные линии формы Visio**
 Фигуры Visio могут наследовать родительский стиль и основную фигуру. Разработчики могут получить или установить наследуемые данные строки формы Visio. Свойство InheritLine, предоставляемое[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class содержит значения форматирования строки для фигуры, наследуемой родительским стилем и основной фигурой.
#### **Пример программирования извлечения унаследованных строковых данных**
Следующий фрагмент кода извлекает унаследованные данные линии фигуры. Пожалуйста, проверьте этот пример кода:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
	Line line = shape.InheritLine;
	Console.WriteLine(line.LinePattern.Value);
	Console.WriteLine(line.LineColor.Value);
	Console.WriteLine(line.BeginArrow.Value);
	Console.WriteLine(line.BeginArrowSize.Value);
	Console.WriteLine(line.EndArrow.Value);
	Console.WriteLine(line.EndArrowSize.Value);
	Console.WriteLine(line.LineWeight.Value);
}

{{< /highlight >}}
```

