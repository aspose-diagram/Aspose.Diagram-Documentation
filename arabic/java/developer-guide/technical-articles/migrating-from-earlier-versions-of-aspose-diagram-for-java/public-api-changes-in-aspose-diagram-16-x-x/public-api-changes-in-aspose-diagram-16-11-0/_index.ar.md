---
title: API عام تغييرات في Aspose.Diagram 16.11.0
type: docs
weight: 20
url: /ar/java/public-api-changes-in-aspose-diagram-16-11-0/
---
{{% alert color="primary" %}} 

يصف هذا المستند التغييرات التي تم إجراؤها على Aspose.Diagram API من الإصدار 6.8.0 إلى 16.11.0 ، والتي قد تهم مطوري الوحدة / التطبيق. لا يشمل فقط الأساليب العامة الجديدة والمحدثة ، بل يشمل أيضًا وصفًا لأي تغييرات في السلوك خلف الكواليس في Aspose.Diagram.

{{% /alert %}} 
### **تعديل خصائص عنصر تحكم ActiveX**
 يمكن للمطورين استرداد عنصر تحكم ActiveX ثم تعديل خصائصه. لقد أضفنا خاصية ActiveXControl في ملف[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) صف دراسي. الرجاء التحقق من مثال هذا الرمز:

**Java**

{{< highlight "csharp" >}}

 // load a Visio diagram

Diagram diagram = new Diagram("C:\\temp\\Drawing1.vsd");

// get a Visio page by name

Page page = diagram.getPages().getPage("Page-1");

// get a shape by ID

Shape shape = page.getShapes().getShape(1);

// get an ActiveX control

CommandButtonActiveXControl cbac = (CommandButtonActiveXControl)shape.getActiveXControl();

// set width of the command button control

cbac.setWidth(4);

// set height of the command button control

cbac.setHeight(4);

// set caption of the command button control

cbac.setCaption("Test Button");

// save diagram

diagram.save("C:\\temp\\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **أدخل شكل نص في Visio Diagram**
يمكن للمطورين إدخال شكل نصي في Visio diagram باستخدام Aspose.Diagram API. الرجاء التحقق من مثال الرمز هذا:

**Java**

{{< highlight "java" >}}

 // create a new diagram

Diagram diagram = new Diagram();

// set parameters

double PinX = 1, PinY = 1, Width = 1, Height = 1;

String text = "Test text";

// add text to a Visio page

diagram.getPages().get(0).addText(PinX, PinY, Width, Height, text);

// save diagram 

diagram.save("C:\\temp\\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
