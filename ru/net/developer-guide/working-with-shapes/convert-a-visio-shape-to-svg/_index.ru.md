---
title: Преобразование формы Visio в Svg
type: docs
weight: 10
url: /ru/net/convert-a-visio-shape-to-svg/
description: В этом разделе объясняется, как преобразовать форму visio в svg с помощью Aspose.Diagram.
---
## ** Преобразование формы visio в svg**
 Метод ToSvg, предоставляемый[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) класс можно использовать для преобразования в svg.

В приведенном ниже коде показано, как:

1. Загрузите образец diagram.
1. получить конкретную страницу.
1. получить определенную форму.
1. преобразовать форму в svg.
### **Форма в SVG**
Используйте следующий код в своем приложении .net, чтобы преобразовать фигуру visio в svg.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToSvg.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

SVGSaveOptions svgOptions = new SVGSaveOptions();
// Shape to Svg
shape.ToSvg("out.svg",svgOptions);

{{< /highlight >}}
```

