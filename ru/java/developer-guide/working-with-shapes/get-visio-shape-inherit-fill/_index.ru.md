---
title: Получить Visio Форма наследует заливку
type: docs
weight: 100
url: /ru/java/get-visio-shape-inherit-fill/
description: В этом разделе объясняется, как получить стиль заливки фигуры visio, унаследованный от ее родительского стиля, и мастер с Aspose.Diagram.
---
### **Получить унаследованные данные заполнения формы Visio**
Фигуры Visio могут наследовать родительский стиль и основную фигуру. Разработчики могут получить наследуемые данные заливки формы Visio. Свойство InheritFill, предоставляемое[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class содержит значения форматирования заливки для фигуры, наследуемой родительским стилем и основной фигурой.
#### **Пример программирования извлечения унаследованных данных заполнения**
Следующий фрагмент кода извлекает унаследованные данные заливки фигуры. Пожалуйста, проверьте этот пример кода:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveInheritedFillData.class) + "Shapes/";

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.getPages().getPage("Page-1");
// Get shape by ID
Shape shape = page.getShapes().getShape(1);
// Get the fill formatting values
System.out.println(shape.getInheritFill().getFillBkgnd().getValue());
System.out.println(shape.getInheritFill().getFillForegnd().getValue());
System.out.println(shape.getInheritFill().getFillPattern().getValue());
System.out.println(shape.getInheritFill().getShapeShdwObliqueAngle().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetX().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetY().getValue());
System.out.println(shape.getInheritFill().getShapeShdwScaleFactor().getValue());
System.out.println(shape.getInheritFill().getShapeShdwType().getValue());
System.out.println(shape.getInheritFill().getShdwBkgnd().getValue());
System.out.println(shape.getInheritFill().getShdwBkgndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwForegnd().getValue());
System.out.println(shape.getInheritFill().getShdwForegndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwPattern().getValue());

{{< /highlight >}}


