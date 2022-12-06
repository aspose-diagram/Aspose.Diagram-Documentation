---
title: تجميع وتحويل والتحقق من الأشكال
type: docs
weight: 80
url: /ar/net/group-convert-and-verify-shapes/
description: يشرح هذا القسم كيفية تجميع الأشكال باستخدام Aspose.Diagram.
---
## **قم بتجميع الأشكال المتعددة معًا في رسم Visio**
Aspose.Diagram API يسمح للمطورين بتجميع الأشكال معًا لنقلها جميعًا مرة واحدة. يحتفظ كل شكل في المجموعة بهوية فريدة وله مجموعة خصائصه الخاصة. عندما نغير تنسيق مجموعة من الأشكال ، فإنه يعين الخاصية الجديدة لكل شكل.
### **كيفية تجميع الأشكال**
 طريقة المجموعة المعروضة من قبل[ShapeCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) يمكن استخدام فئة لتجميع الأشكال معًا.

يوضح الكود أدناه كيفية:

1. تحميل عينة diagram.
1. تهيئة مجموعة من الأشكال
1. الحصول على شكل معين بواسطة معرف.
1. الحصول على شكل معين آخر بواسطة معرف.
1. تعيين الأشكال للمصفوفة.
1. تجميع الأشكال عن طريق استدعاء طريقة المجموعة.
1. احفظ diagram
#### **عينة برمجة الأشكال الجماعية**
استخدم الكود التالي في تطبيق .NET لتجميع الأشكال معًا باستخدام Aspose.Diagram for .NET API.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-GroupShapes-GroupShapes.cs" >}}
## **تحويل شكل Visio إلى تنسيقات ملفات أخرى**
Aspose.Diagram for .NET API يسمح للمطورين بتحويل شكل Visio واحد إلى أي تنسيق ملف آخر مدعوم. في هذه المقالة ، نقوم بإزالة جميع أشكال Visio الأخرى من الصفحة وتخصيص إعداد الصفحة وفقًا لحجم الشكل المصدر.
### **تحويل شكل Visio معين**
 يمكن للمطورين تحويل شكل Visio إلى PDF و HTML و Image و SVG و SWF بواسطة**تحديد خيارات الحفظ Visio**.
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
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SaveVisioShapeInOtherFormats-SaveVisioShapeInOtherFormats.cs" >}}
### **تحويل Visio الشكل إلى PDF**
تسمح طريقة ToPdf لفئة الشكل بتحويل شكل إلى تنسيق PDF.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **تحويل Visio الشكل إلى HTML**
تسمح طريقة ToHTML لفئة الشكل بتحويل شكل إلى تنسيق HTML.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}
## **تحقق مما إذا كان شكلا Visio متصل أو ملتصق**
 Aspose.Diagram for .NET API يسمح للمطورين بالتحقق من أن الشكلين Visio ملتصقان أو متصلان. في السابق ، رأينا كيف يمكننا توصيل شكلين أو لصقهما في موضوعات المساعدة هذه:[إضافة وتوصيل Visio الأشكال](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) و[أشكال الغراء داخل الحاوية](/diagram/ar/net/working-with-shapes-gluing/).
### **التحقق من الأشكال المتصلة أو الملصقة**
 ال[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) تقدم الفئة خصائص IsGlued و IsConnected لتحديد ما إذا كان الشكلين ملتصقين أم متصلين.
#### **التحقق من نموذج برمجة الأشكال المتصلة أو الملصقة**
يتحقق الجزء التالي من الكود مما إذا كان الشكلين متصلين أم تم لصقهما.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-VerifyConnectedOrGluedShapes-VerifyConnectedOrGluedShapes.cs" >}}
## **تحقق مما إذا كان الشكل Visio في مجموعة من الأشكال**
Aspose.Diagram for .NET API يسمح للمطورين بالتحقق من أن الشكل Visio موجود في مجموعة من الأشكال أم لا.
### **التحقق من الشكل في مجموعة الأشكال**
ال[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)تقدم الفئة خصائص IsInGroup لتحديد ما إذا كان الشكل Visio في شكل مجموعة.
#### **التحقق من الشكل في عينة برمجة مجموعة الأشكال**
يتحقق جزء التعليمات البرمجية التالي مما إذا كان الشكل في شكل مجموعة.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-VerifyShapeIsInGroup-VerifyShapeIsInGroup.cs" >}}
