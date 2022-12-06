---
title: عام API تغييرات في Aspose.Diagram 16.12.0
type: docs
weight: 10
url: /ar/net/public-api-changes-in-aspose-diagram-16-12-0/
---
{{% alert color="primary" %}} 

يصف هذا المستند التغييرات التي تم إجراؤها على Aspose.Diagram API من الإصدار 16.11.0 إلى 16.12.0 ، والتي قد تهم مطوري الوحدة / التطبيق. لا يشمل فقط الأساليب العامة الجديدة والمحدثة ، بل يشمل أيضًا وصفًا لأي تغييرات في السلوك خلف الكواليس في Aspose.Diagram.

{{% /alert %}} 
## **تعديل خصائص التدرج اللوني**
يمكن للمطورين استرداد نقطة توقف متدرجة ثم تعديل خصائصها. لقد أضفنا[ملء الانحدار](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientfill)و[التدرج](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientstop)فصول لهذه الأغراض. يرجى التحقق من مثال الرمز:

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
