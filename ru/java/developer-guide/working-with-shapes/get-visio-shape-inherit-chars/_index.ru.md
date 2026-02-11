---
title: Получить Visio Shape Inherit Charts
type: docs
weight: 101
url: /ru/java/get-visio-shape-inherit-chars/
description: В этом разделе объясняется, как получить стиль шрифта фигуры visio, унаследованный от его родительского стиля, и мастер с Aspose.Diagram.
---
### **Получить унаследованные данные шрифта формы Visio**
 Фигуры Visio могут наследовать родительский стиль и основную фигуру. Разработчики могут получить или установить наследуемые данные шрифта формы Visio. Свойство InheritChars, предоставляемое[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class содержит значения шрифта для фигуры, наследуемой родительским стилем и основной фигурой.
#### **Пример программирования извлечения унаследованных данных шрифта**
Следующий фрагмент кода извлекает унаследованные данные шрифта фигуры. Пожалуйста, проверьте этот пример кода:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveInheritedChars.class) + "Shapes/";

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.getPages().getPage("Page-1");
// Get shape by ID
Shape shape = page.getShapes().getShape(1);
//Get Inherit Chars from the parent style and master
CharCollection chars = shape.getInheritChars();
for (int j = 0; j < chars.getCount(); j++) 
{
	Char ch = chars.get(j);
	System.out.println(ch.getColor().getValue());
	System.out.println(ch.getColorTrans().getValue());
	System.out.println(ch.getFontScale().getValue());
	System.out.println(ch.getSize().getValue());
	System.out.println(ch.getStyle().getValue());
	System.out.println(ch.getFontName().getValue());
	System.out.println(ch.isBold());
	System.out.println(ch.isDoubleStrikethrough());
	System.out.println(ch.isDoubleUnderline());
	System.out.println(ch.isItalic());
	System.out.println(ch.isStrikethrough());
	System.out.println(ch.isSubscript());
	System.out.println(ch.isSuperscript());
	System.out.println(ch.isUnderline());
}

{{< /highlight >}}




