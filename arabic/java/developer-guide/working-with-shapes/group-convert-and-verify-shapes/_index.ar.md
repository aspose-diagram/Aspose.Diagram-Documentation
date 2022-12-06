---
title: تجميع وتحويل والتحقق من الأشكال
type: docs
weight: 50
url: /ar/java/group-convert-and-verify-shapes/
---
## **قم بتجميع الأشكال المتعددة معًا في رسم Visio**
Aspose.Diagram API يسمح للمطورين بتجميع الأشكال معًا لنقلها جميعًا مرة واحدة. يحتفظ كل شكل في المجموعة بهوية فريدة وله مجموعة خصائصه الخاصة. عندما نغير تنسيق مجموعة من الأشكال ، فإنه يعين الخاصية الجديدة لكل شكل.
### **كيفية تجميع الأشكال**
يمكن استخدام طريقة المجموعة التي تعرضها فئة ShapeCollection لتجميع الأشكال معًا.

يوضح الكود أدناه كيفية:

1. تحميل عينة diagram.
1. تهيئة مجموعة من الأشكال
1. الحصول على شكل معين بواسطة معرف.
1. الحصول على شكل معين آخر بواسطة معرف.
1. تعيين الأشكال للمصفوفة.
1. تجميع الأشكال عن طريق استدعاء طريقة المجموعة.
1. احفظ diagram
#### **عينة برمجة الأشكال الجماعية**
استخدم الكود التالي في تطبيق Java لتجميع الأشكال معًا باستخدام Aspose.Diagram for Java API.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-GroupShapes-GroupShapes.java" >}}
## **تحويل شكل Visio إلى تنسيقات ملفات أخرى**
Aspose.Diagram for Java API يسمح للمطورين بتحويل شكل Visio واحد إلى أي تنسيق ملف آخر مدعوم. في هذه المقالة ، نقوم بإزالة جميع أشكال Visio الأخرى من الصفحة وتخصيص إعداد الصفحة وفقًا لحجم الشكل المصدر.
### **تحويل شكل Visio معين**
 يمكن للمطورين تحويل شكل Visio إلى PDF و HTML و Image و SVG و SWF بواسطة[تحديد خيارات الحفظ Visio]().
يعمل رمز المثال هذا على النحو التالي:

1. قم بتحميل المصدر Visio.
1. احصل على صفحة معينة.
1. قم بإزالة صفحة الخلفية.
1. قم بإنشاء جدول تجزئة لجميع الأشكال التي تحتوي على المعرفات والأسماء.
1. كرر من خلال جدول التجزئة
1. قم بإزالة كافة الأشكال من صفحة Visio ، باستثناء الشكل المعين.
1. اضبط حجم الصفحة.
1. احفظ الصفحة Visio بأي تنسيق ملف مدعوم.
#### **تحويل نموذج برمجة الشكل**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SaveVisioShapeInOtherFormats-SaveVisioShapeInOtherFormats.java" >}}
### **حوّل Visio إلى PDF**
تسمح طريقة ToPdf لفئة الشكل بتحويل شكل إلى تنسيق PDF.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **حوّل Visio إلى HTML**
تسمح طريقة ToHTML لفئة الشكل بتحويل شكل إلى تنسيق HTML.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

HTMLSaveOptions hs = new HTMLSaveOptions();

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}

{{% alert color="primary" %}} 

 نرحب باستفساراتكم واقتراحاتكم على[Aspose.Diagram المنتدى](https://forum.aspose.com/c/diagram/17). سوف نقوم بالرد على الفور.

{{% /alert %}} 
## **تحقق مما إذا كان شكلا Visio متصل أو ملتصق**
 Aspose.Diagram for Java API يسمح للمطورين بالتحقق من أن الشكلين Visio ملتصقان أو متصلان. في السابق ، رأينا كيف يمكننا توصيل شكلين أو لصقهما في موضوعات المساعدة هذه:[إضافة وتوصيل Visio الأشكال](/diagram/ar/java/add-and-connect-visio-shapes/) و[أشكال الغراء داخل الحاوية](/diagram/ar/java/working-with-shapes-gluing/).
### **التحقق من الأشكال المتصلة أو الملصقة**
 ال[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) تقدم الفئة خصائص IsGlued و IsConnected لتحديد ما إذا كان الشكلين ملتصقين أم متصلين.
#### **التحقق من نموذج برمجة الأشكال المتصلة أو الملصقة**
يتحقق الجزء التالي من الكود مما إذا كان الشكلين متصلين أم تم لصقهما.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-VerifyConnectedOrGluedShapes-VerifyConnectedOrGluedShapes.java" >}}
## **تحقق مما إذا كان الشكل Visio في مجموعة من الأشكال**
Aspose.Diagram for Java API يسمح للمطورين بالتحقق من أن الشكل Visio موجود في مجموعة من الأشكال أم لا.
### **التحقق من الشكل في مجموعة الأشكال**
توفر فئة الشكل خصائص IsInGroup لتحديد ما إذا كان الشكل Visio في شكل مجموعة.
#### **التحقق من الشكل في عينة برمجة مجموعة الأشكال**
يتحقق جزء التعليمات البرمجية التالي مما إذا كان الشكل في شكل مجموعة.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-VerifyShapeIsInGroup-VerifyShapeIsInGroup.java" >}}

{{% alert color="primary" %}} 

 نرحب باستفساراتكم واقتراحاتكم على[Aspose.Diagram المنتدى](https://forum.aspose.com/c/diagram/17). سوف نقوم بالرد على الفور.

{{% /alert %}}
