---
title: Получить Visio Shape Inherit Charts
type: docs
weight: 101
url: /ru/net/get-visio-shape-inherit-chars/
description: В этом разделе объясняется, как получить стиль шрифта фигуры visio, унаследованный от его родительского стиля, и мастер с Aspose.Diagram.
---
### **Получить унаследованные данные шрифта формы Visio**
 Фигуры Visio могут наследовать родительский стиль и основную фигуру. Разработчики могут получить или установить наследуемые данные шрифта формы Visio. Свойство InheritLine, предоставляемое[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class содержит значения форматирования строки для фигуры, наследуемой родительским стилем и основной фигурой.
#### **Пример программирования извлечения унаследованных данных шрифта**
Следующий фрагмент кода извлекает унаследованные данные шрифта фигуры. Пожалуйста, проверьте этот пример кода:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
	Aspose.Diagram.Char ch = shape.InheritChars.GetChar(0);
	Console.WriteLine(ch.Style.Value);
	Console.WriteLine(ch.Color.Value); 
	Console.WriteLine(ch.FontName.Value); 
	Console.WriteLine(ch.Size.Value);
	Console.WriteLine(ch.Case.Value);
	Console.WriteLine(ch.IsUnderline);
	Console.WriteLine(ch.IsItalic);
	Console.WriteLine(ch.IsStrikethrough);
	Console.WriteLine(ch.IsDoubleStrikethrough);
	Console.WriteLine(ch.IsSubscript);
	Console.WriteLine(ch.IsSuperscript); 
}

{{< /highlight >}}


