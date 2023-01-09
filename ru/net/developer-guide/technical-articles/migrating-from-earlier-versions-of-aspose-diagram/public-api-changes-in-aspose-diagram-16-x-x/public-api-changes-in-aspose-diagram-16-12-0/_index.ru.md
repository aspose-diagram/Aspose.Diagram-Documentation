---
title: Общедоступный API Изменения в Aspose.Diagram 16.12.0
type: docs
weight: 10
url: /ru/net/public-api-changes-in-aspose-diagram-16-12-0/
---
{{% alert color="primary" %}} 

В этом документе описаны изменения в Aspose.Diagram API с версии 16.11.0 до 16.12.0, которые могут представлять интерес для разработчиков модулей/приложений. Он включает в себя не только новые и обновленные общедоступные методы, но и описание любых изменений в поведении за кулисами в Aspose.Diagram.

{{% /alert %}} 
## **Изменить свойства градиента**
Разработчики могут получить точку градиента, а затем изменить ее свойства. Мы добавили[Градиентная заливка](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientfill)а также[ГрадиентСтоп](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientstop)классы для этих целей. Пожалуйста, проверьте пример кода:

**C#**

{{< highlight "csharp" >}}

 // load a Visio drawing

Diagram diagram = new Diagram(@"C:\temp\MyVisio.vsdx");

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

diagram.Save(@"C:\temp\Output.pdf", SaveFileFormat.PDF);

{{< /highlight >}}
