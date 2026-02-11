---
title: Получить Visio Строку наследования формы
type: docs
weight: 100
url: /ru/java/get-visio-shape-inherit-line/
description: В этом разделе объясняется, как получить стиль линии фигуры visio, унаследованный от его родительского стиля, и мастер с Aspose.Diagram.
---
### **Получить унаследованные данные линии формы Visio**
 Фигуры Visio могут наследовать родительский стиль и основную фигуру. Разработчики могут получить или установить наследуемые данные строки формы Visio. Свойство InheritLine, предоставляемое[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class содержит значения форматирования строки для фигуры, наследуемой родительским стилем и основной фигурой.
#### **Пример программирования извлечения унаследованных строковых данных**
Следующий фрагмент кода извлекает унаследованные данные линии фигуры. Пожалуйста, проверьте этот пример кода:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveInheritedLine.class) + "Shapes/";

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.getPages().getPage("Page-1");
// Get shape by ID
Shape shape = page.getShapes().getShape(1);
//Get Inherit Line from the parent style and master
Line line = shape.getInheritLine();
// Get the line formatting values
System.out.println(line.getBeginArrow().getValue());
System.out.println(line.getBeginArrowSize().getValue());
System.out.println(line.getEndArrow().getValue());
System.out.println(line.getEndArrowSize().getValue());
System.out.println(line.getLineColor().getValue());
System.out.println(line.getLinePattern().getValue());
System.out.println(line.getLineWeight().getValue());
System.out.println(line.getRounding().getValue());

{{< /highlight >}}


