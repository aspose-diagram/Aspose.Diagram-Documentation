---
title: Изменение градиента фигуры Visio
type: docs
weight: 10
url: /ru/net/modify-the-gradient-of-a-visio-shape/
description: На этой странице описывается, как изменить цвет градиента фигуры visio с помощью библиотеки Aspose.Diagram.
---
{{% alert color="primary" %}} 

Используя Aspose.Diagram API, разработчики могут улучшить внешний вид фигуры Visio, изменив свойства градиента. Разработчики могут получить градиентную заливку, чтобы установить направление, угол, цвет остановки градиента и положение и т. д.

{{% /alert %}} 
## **Изменение примера программирования градиентной заливки**
[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)класс предлагает свойство Fill, которое позволяет разработчикам извлекать[Градиентная заливка](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientfill)объект. Класс GradientFill содержит данные градиента фигуры Visio. Разработчики могут установить все его доступные свойства, а также получить точку градиента по индексу, чтобы установить свойства цвета и положения.

```
{{< highlight "csharp" >}}
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeGradientFillData();
// Load the Visio diagram
Diagram diagram = new Diagram(dataDir + "ShapewithGradientFill.vsdx");
// get page by name
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");
// get shape by ID
Aspose.Diagram.Shape shape = page.Shapes.GetShape(1);
// get the gradient fill properties
GradientFill gradientfill = shape.Fill.GradientFill;
// get the gradient stops
GradientStopCollection stops = gradientfill.GradientStops;
// get the gradient stop by index
GradientStop stop = stops[0];
// set gradient stop properties
stop.Color.Ufe.F = "";
stop.Position.Value = 0.5;
gradientfill.GradientDir.Value = (int)GradientFillDir.RectangleFromBottomRight;
gradientfill.GradientAngle.Value = 0.7853981633974501;
// save the Visio drawing
diagram.Save(dataDir + "ShapewithGradientFill_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
