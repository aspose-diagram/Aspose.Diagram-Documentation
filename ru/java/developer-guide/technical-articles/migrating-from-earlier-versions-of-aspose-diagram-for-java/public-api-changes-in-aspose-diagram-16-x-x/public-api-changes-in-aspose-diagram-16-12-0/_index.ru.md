---
title: Общедоступный API Изменения в Aspose.Diagram 16.12.0
type: docs
weight: 10
url: /ru/java/public-api-changes-in-aspose-diagram-16-12-0/
---
{{% alert color="primary" %}} 

В этом документе описаны изменения в Aspose.Diagram API с версии 16.11.0 до 16.12.0, которые могут представлять интерес для разработчиков модулей/приложений. Он включает в себя не только новые и обновленные общедоступные методы, но и описание любых изменений в поведении за кулисами в Aspose.Diagram.

{{% /alert %}} 
### **Изменить свойства градиента**
Разработчики могут получить точку градиента, а затем изменить ее свойства. Мы добавили[Градиентная заливка](https://reference.aspose.com/diagram/java/com.aspose.diagram/gradientfill)а также[ГрадиентСтоп](https://reference.aspose.com/diagram/java/com.aspose.diagram/gradientstop)классы для этих целей. Пожалуйста, проверьте пример кода:

**Java**

{{< highlight "csharp" >}}

 // load a Visio drawing

Diagram diagram = new Diagram("C:\\temp\\MyVisio.vsdx");

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

diagram.save("C:\\temp\\Output.pdf", SaveFileFormat.PDF);

{{< /highlight >}}
