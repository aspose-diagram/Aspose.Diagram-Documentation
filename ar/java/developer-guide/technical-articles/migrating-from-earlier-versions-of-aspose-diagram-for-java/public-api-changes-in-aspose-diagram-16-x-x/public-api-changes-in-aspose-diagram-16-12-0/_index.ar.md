---
title: عام API تغييرات في Aspose.Diagram 16.12.0
type: docs
weight: 10
url: /ar/java/public-api-changes-in-aspose-diagram-16-12-0/
---
{{% alert color="primary" %}} 

يصف هذا المستند التغييرات التي تم إجراؤها على Aspose.Diagram API من الإصدار 16.11.0 إلى 16.12.0 ، والتي قد تهم مطوري الوحدة / التطبيق. لا يشمل فقط الأساليب العامة الجديدة والمحدثة ، بل يشمل أيضًا وصفًا لأي تغييرات في السلوك خلف الكواليس في Aspose.Diagram.

{{% /alert %}} 
### **تعديل خصائص التدرج اللوني**
يمكن للمطورين استرداد نقطة توقف متدرجة ثم تعديل خصائصها. لقد أضفنا[ملء الانحدار](https://reference.aspose.com/diagram/java/com.aspose.diagram/gradientfill)و[التدرج](https://reference.aspose.com/diagram/java/com.aspose.diagram/gradientstop)فصول لهذه الأغراض. يرجى التحقق من مثال الرمز:

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
