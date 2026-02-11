---
title: Получить Visio Форма наследует заливку
type: docs
weight: 100
url: /ru/net/get-visio-shape-inherit-fill/
description: В этом разделе объясняется, как получить стиль заливки фигуры visio, унаследованный от ее родительского стиля, и мастер с Aspose.Diagram.
---
### **Получить унаследованные данные заполнения формы Visio**
Фигуры Visio могут наследовать родительский стиль и основную фигуру. Разработчики могут получить наследуемые данные заливки формы Visio. Свойство InheritFill, предоставляемое[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class содержит значения форматирования заливки для фигуры, наследуемой родительским стилем и основной фигурой.
#### **Пример программирования извлечения унаследованных данных заполнения**
Следующий фрагмент кода извлекает унаследованные данные заливки фигуры. Пожалуйста, проверьте этот пример кода:

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
	Fill f = shape.InheritFill;
	Console.WriteLine(f.FillForegnd.Value);
	Console.WriteLine(f.FillPattern.Value);
	Console.WriteLine(f.ShdwForegnd.Value);
	Console.WriteLine(f.ShdwPattern.Value);
}

{{< /highlight >}}
```

