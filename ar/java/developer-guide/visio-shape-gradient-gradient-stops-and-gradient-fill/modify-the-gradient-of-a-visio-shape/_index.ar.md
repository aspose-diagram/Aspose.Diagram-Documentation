---
title: قم بتعديل التدرج اللوني لشكل Visio
type: docs
weight: 10
url: /ar/java/modify-the-gradient-of-a-visio-shape/
---
{{% alert color="primary" %}} 

باستخدام Aspose.Diagram API ، يمكن للمطورين تحسين مظهر الشكل Visio عن طريق تعديل خصائص التدرج. يمكن للمطورين استرداد تعبئة متدرجة لتعيين الاتجاه والزاوية ولون إيقاف التدرج والموضع وما إلى ذلك.

{{% /alert %}} 
## **تعديل نموذج برمجة التعبئة المتدرجة**
[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)تقدم class خاصية Fill التي تتيح للمطورين استرداد ملف[ملء الانحدار](https://reference.aspose.com/diagram/java/com.aspose.diagram/gradientfill)هدف. تحتوي فئة GradientFill على بيانات التدرج اللوني لشكل Visio. يمكن للمطورين تعيين جميع خصائصه المتاحة وكذلك استرداد نقطة توقف التدرج بفهرس لتعيين خصائص اللون والموضع.


{{< highlight java >}}
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

