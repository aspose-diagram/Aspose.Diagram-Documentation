---
title: إنشاء وتخطيط وملاءمة تلقائية الأشكال
type: docs
weight: 10
url: /ar/java/create-layout-and-auto-fit-shapes/
---
## **إنشاء Diagram**
 يتيح لك Aspose.Diagram for Java قراءة وإنشاء Microsoft Visio الرسوم التخطيطية من داخل التطبيقات الخاصة بك ، بدون أتمتة Microsoft Office. الخطوة الأولى عند تكوين وثائق جديدة هي تكوين diagram. ثم[إضافة الأشكال والموصلات](/diagram/ar/java/add-and-connect-visio-shapes/)لإنشاء diagram. استخدم المُنشئ الافتراضي لـ[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) فئة لإنشاء diagram جديد.
### **عينة البرمجة**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-CreateDiagram-CreateDiagram.java" >}}
## **أشكال التخطيط في نمط المخطط الانسيابي**
 مع أنواع معينة من الرسومات المتصلة ، مثل المخططات الانسيابية والرسومات التخطيطية للشبكة ، يمكنك استخدام ملحق**أشكال التخطيط** ميزة لوضع الأشكال تلقائيًا. يعد تحديد المواقع تلقائيًا أسرع من سحب كل شكل يدويًا إلى موقع جديد.

على سبيل المثال ، إذا كنت تقوم بتحديث مخطط انسيابي كبير لتضمين عملية جديدة ، فيمكنك إضافة الأشكال التي تشكل العملية وتوصيلها ، ثم استخدام ميزة التخطيط لتخطيط الرسم المحدث تلقائيًا.

 طريقة Layout ، المكشوفة بواسطة ملف[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) تخطيطات الفصل للأشكال و / أو إعادة توجيه الموصلات على جميع صفحات diagram. يقبل هذا الأسلوب كائن LayoutOptions كوسيطة. استخدم الخصائص المختلفة المعروضة بواسطة فئة LayoutOptions لتخطيط الأشكال تلقائيًا.

توضح الصورة أدناه diagram الذي تم تحميله بواسطة مقتطفات التعليمات البرمجية في هذه المقالة ، قبل تطبيق التخطيط التلقائي. توضح مقتطفات التعليمات البرمجية كيفية التقديم[تخطيطات مخطط انسيابي](/diagram/ar/java/create-2c-layout-and-auto-fit-shapes/) و[تخطيطات الشجرة المدمجة](/diagram/ar/java/create-2c-layout-and-auto-fit-shapes/).

**المصدر diagram.** 

![ما يجب القيام به: image_بديل_نص](create-layout-and-auto-fit-shapes_1.png)

تأخذ مقتطفات التعليمات البرمجية في هذه المقالة المصدر diagram وتطبق عدة أنواع من التخطيط التلقائي عليها ، مع حفظ كل منها في ملف منفصل.

|<p>**تخطيط الأشكال من الأسفل إلى الأعلى** </p><p>![ما يجب القيام به: image_بديل_نص](create-layout-and-auto-fit-shapes_2.png)</p>|<p>**تخطيط الأشكال من أعلى إلى أسفل** </p><p>![ما يجب القيام به: image_بديل_نص](create-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**تخطيط الأشكال من اليسار إلى اليمين** </p><p>![ما يجب القيام به: image_بديل_نص](create-layout-and-auto-fit-shapes_4.png)</p>|<p>**تخطيط الأشكال من اليمين إلى اليسار** </p><p>![ما يجب القيام به: image_بديل_نص](create-layout-and-auto-fit-shapes_5.png)</p>|
لتخطيط الأشكال في نمط المخطط الانسيابي:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم بإنشاء مثيل لفئة LayoutOptions وقم بتعيين الخصائص ذات الصلة بنمط المخطط الانسيابي.
1. قم باستدعاء أسلوب تخطيط الفئة Diagram عن طريق تمرير LayoutOptions.
1. اتصل بـ Diagram class 'طريقة Save لكتابة رسم Visio.
### **عينة برمجة نمط المخطط الانسيابي**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-LayOutShapesInFlowchartStyle-LayOutShapesInFlowchartStyle.java" >}}
### **تخطيط الأشكال في نمط الشجرة المضغوطة**
 يحاول نمط تخطيط الشجرة المضغوط بناء هيكل شجرة. يستخدم نفس ملف الإدخال مثل ملف[المثال أعلاه](/diagram/ar/java/create-2c-layout-and-auto-fit-shapes/)ويحفظ في العديد من أنماط الأشجار المدمجة المختلفة.

|<p>**تخطيط شجرة مضغوط - لأسفل ولليمين** </p><p>![ما يجب القيام به: image_بديل_نص](create-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**تخطيط شجرة مضغوط - لأسفل ولليسار** </p><p>![ما يجب القيام به: image_بديل_نص](create-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**تخطيط شجرة مضغوط - لليمين ولأسفل** </p><p>![ما يجب القيام به: image_بديل_نص](create-layout-and-auto-fit-shapes_8.png)</p>|<p>**تخطيط شجرة مضغوط - لليسار ولأسفل** </p><p>![ما يجب القيام به: image_بديل_نص](create-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
لتخطيط الأشكال في نمط الشجرة المدمجة:

1.  قم بإنشاء مثيل لـ[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) صف دراسي.
1. قم بإنشاء مثيل لفئة LayoutOptions وقم بتعيين خصائص نمط الشجرة المدمجة.
1. قم باستدعاء أسلوب تخطيط الفئة Diagram عن طريق تمرير LayoutOptions.
1. قم باستدعاء الأسلوب Save للفئة Diagram لكتابة ملف Visio.
#### **عينة برمجة نمط الشجرة المدمجة**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-LayOutShapesInCompactTreeStyle-LayOutShapesInCompactTreeStyle.java" >}}
## **احتواء تلقائي Visio Diagram**
Aspose.Diagram API يدعم التركيب التلقائي للرسم Visio. تساعد عملية الميزة هذه على إحضار الأشكال الخارجية داخل حدود الصفحة Visio.

Aspose.Diagram for Java API له الفئة Diagram التي تمثل رسم Visio. تعرض الفئة DiagramSaveOptions خاصية AutoFitPageToDrawingContent لتلائم رسم Visio تلقائيًا.

هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. قم بإنشاء كائن من فئة DiagramSaveOptions وتمرير تنسيق الملف الناتج.
1. قم بتعيين خاصية AutoFitPageToDrawingContent للكائن DiagramSaveOptions.
1. استدعاء طريقة حفظ لكائن الفئة Diagram وأيضا تمرير مسار الملف الكامل وكائن DiagramSaveOptions.
### **عينة البرمجة الملائمة التلقائية**
يوضح رمز المثال التالي كيفية احتواء الأشكال تلقائيًا في Visio diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-AutoFitShapesInVisio-AutoFitShapesInVisio.java" >}}
## **العمل مع مشروع VBA**
### **تعديل كود وحدة VBA في Visio Diagram**
توضح هذه المقالة كيفية تعديل رمز الوحدة النمطية لـ VBA تلقائيًا باستخدام Aspose.Diagram for Java.

لقد أضفنا فئات VbaModule و VbaModuleCollection و VbaProject و VbaProjectReference و VbaProjectReferenceCollection. تساعد هذه الفئات في التحكم في مشروع VBA. يمكن للمطورين استخراج وتعديل رمز الوحدة النمطية لـ VBA.
### **تعديل نموذج برمجة رمز الوحدة النمطية لـ VBA**
الرجاء التحقق من مثال هذا الرمز:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-ModifyVBAModuleCode-ModifyVBAModuleCode.java" >}}
### **قم بإزالة كافة وحدات الماكرو من Visio Diagram**
Aspose.Diagram for Java يسمح للمطورين بإزالة كافة وحدات الماكرو من Visio diagram.

خاصية JavaProjectData ، المكشوفة بواسطة ملف[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class ، تسمح لك بإزالة كافة وحدات الماكرو من الرسم Visio.
### **قم بإزالة كافة نماذج برمجة وحدات الماكرو**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-RemoveMacrosFromVisio-RemoveMacrosFromVisio.java" >}}
