---
title: قم بتعديل التدرج اللوني لشكل Visio
type: docs
weight: 10
url: /ar/net/modify-the-gradient-of-a-visio-shape/
description: توضح هذه الصفحة كيفية تعديل لون التدرج لشكل visio باستخدام مكتبة Aspose.Diagram.
---
{{% alert color="primary" %}} 

باستخدام Aspose.Diagram API ، يمكن للمطورين تحسين مظهر الشكل Visio عن طريق تعديل خصائص التدرج. يمكن للمطورين استرداد تعبئة متدرجة لتعيين الاتجاه والزاوية ولون إيقاف التدرج والموضع وما إلى ذلك.

{{% /alert %}} 
## **تعديل نموذج برمجة التعبئة المتدرجة**
[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)تقدم class خاصية Fill التي تتيح للمطورين استرداد ملف[ملء الانحدار](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientfill)هدف. تحتوي فئة GradientFill على بيانات التدرج اللوني لشكل Visio. يمكن للمطورين تعيين جميع خصائصه المتاحة وكذلك استرداد نقطة توقف التدرج بفهرس لتعيين خصائص اللون والموضع.


{{< highlight csharp >}}
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

