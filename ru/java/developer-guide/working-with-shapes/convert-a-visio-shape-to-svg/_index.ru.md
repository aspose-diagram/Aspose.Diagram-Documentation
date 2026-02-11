---
title: Преобразование формы Visio в Svg
type: docs
weight: 10
url: /ru/java/convert-a-visio-shape-to-svg/
description: В этом разделе объясняется, как преобразовать форму visio в svg с помощью Aspose.Diagram.
---
## ** Преобразование формы visio в svg**
 Метод ToSvg, предоставляемый[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) класс можно использовать для преобразования в svg.

В приведенном ниже коде показано, как:

1. Загрузите образец diagram.
1. получить конкретную страницу.
1. получить определенную форму.
1. преобразовать форму в svg.
### **Форма в SVG**
Используйте следующий код в своем Java-приложении, чтобы преобразовать фигуру visio в svg.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ShapeToSvg.class); 
// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToSvg.vsdx");

// Get a particular page
Page page = diagram.getPages().get(0);

// Get a particular shape
Shape shape = page.getShapes().get(0);

// Shape to Svg
SVGSaveOptions option = new SVGSaveOptions();
shape.toSvg("out.svg",option);
{{< /highlight >}}
```


