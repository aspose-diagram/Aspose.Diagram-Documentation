---
title: Изменение градиента фигуры Visio
type: docs
weight: 10
url: /ru/java/modify-the-gradient-of-a-visio-shape/
---
{{% alert color="primary" %}} 

Используя Aspose.Diagram API, разработчики могут улучшить внешний вид фигуры Visio, изменив свойства градиента. Разработчики могут получить градиентную заливку, чтобы установить направление, угол, цвет остановки градиента и положение и т. д.

{{% /alert %}} 
## **Изменение примера программирования градиентной заливки**
[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)класс предлагает свойство Fill, которое позволяет разработчикам извлекать[Градиентная заливка](https://reference.aspose.com/diagram/java/com.aspose.diagram/gradientfill)объект. Класс GradientFill содержит данные градиента фигуры Visio. Разработчики могут установить все его доступные свойства, а также получить точку градиента по индексу, чтобы установить свойства цвета и положения.

```
{{< highlight "java" >}}
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(ModifyShapeGradientFill.class) + "ShapeGradientFill\\";

// load a Visio drawing
Diagram diagram = new Diagram(dataDir + "ShapewithGradientFill.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by ID
Shape shape = page.getShapes().getShape(1);
// get the gradient fill properties
GradientFill gradientfill = shape.getFill().getGradientFill();
// get the gradient stops
GradientStopCollection stops = gradientfill.getGradientStops();
// get the gradient stop by index
GradientStop stop = stops.get(0);
// set gradient stop properties
stop.getColor().getUfe().setF("");
stop.getPosition().setValue(0.5);
gradientfill.getGradientDir().setValue(GradientFillDir.RECTANGLE_FROM_BOTTOM_RIGHT);
gradientfill.getGradientAngle().setValue(0.7853981633974501);
// save the Visio drawing
diagram.save(dataDir + "ShapewithGradientFill_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}
```
