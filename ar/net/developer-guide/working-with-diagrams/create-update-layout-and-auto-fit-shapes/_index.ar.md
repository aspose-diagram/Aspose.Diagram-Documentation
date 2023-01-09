---
title: إنشاء وتحديث وتخطيط وملاءمة تلقائية الأشكال
type: docs
weight: 10
url: /ar/net/create-update-layout-and-auto-fit-shapes/
description: استخدم C# Diagram API لإنشاء أشكال التخطيط التلقائي وتحديثها في ملفات Visio باستخدام C# داخل تطبيقاتك. دليل كامل مع C# عينات كود.
---
## **إنشاء Diagram**
 يتيح لك Aspose.Diagram for .NET قراءة وإنشاء Microsoft Visio الرسوم التخطيطية من داخل التطبيقات الخاصة بك ، بدون أتمتة Microsoft Office. الخطوة الأولى عند تكوين وثائق جديدة هي تكوين diagram. ثم[إضافة الأشكال والموصلات](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/)لإنشاء diagram. استخدم المُنشئ الافتراضي لـ[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) فئة لإنشاء diagram جديد.
### **عينة البرمجة**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-CreateDiagram-CreateDiagram.cs" >}}
## **أشكال التخطيط في نمط المخطط الانسيابي**
 مع أنواع معينة من الرسومات المتصلة ، مثل المخططات الانسيابية والرسومات التخطيطية للشبكة ، يمكنك استخدام ملحق**أشكال التخطيط** ميزة لوضع الأشكال تلقائيًا. يعد تحديد المواقع تلقائيًا أسرع من سحب كل شكل يدويًا إلى موقع جديد.

على سبيل المثال ، إذا كنت تقوم بتحديث مخطط انسيابي كبير لتضمين عملية جديدة ، فيمكنك إضافة الأشكال التي تشكل العملية وتوصيلها ، ثم استخدام ميزة التخطيط لتخطيط الرسم المحدث تلقائيًا.

 طريقة Layout ، المكشوفة بواسطة ملف[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) تخطيطات الفصل للأشكال و / أو إعادة توجيه الموصلات على جميع صفحات diagram. هذه الطريقة تقبل ملف[خيارات التخطيط](https://reference.aspose.com/diagram/net/aspose.diagram.autolayout/layoutoptions)الكائن كحجة. استخدم الخصائص المختلفة المعروضة بواسطة فئة LayoutOptions لتخطيط الأشكال تلقائيًا.

توضح الصورة أدناه diagram الذي تم تحميله بواسطة مقتطفات التعليمات البرمجية في هذه المقالة ، قبل تطبيق التخطيط التلقائي. توضح مقتطفات التعليمات البرمجية كيفية التقديم[تخطيطات مخطط انسيابي](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) و[تخطيطات الشجرة المدمجة](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/).

**المصدر diagram.**

![ما يجب القيام به: image_بديل_نص](create-update-layout-and-auto-fit-shapes_1.png)

تأخذ مقتطفات التعليمات البرمجية في هذه المقالة المصدر diagram وتطبق عدة أنواع من التخطيط التلقائي عليها ، مع حفظ كل منها في ملف منفصل.

|<p>**تخطيط الأشكال من الأسفل إلى الأعلى** </p><p>![ما يجب القيام به: image_بديل_نص](create-update-layout-and-auto-fit-shapes_2.png)</p>|<p>**تخطيط الأشكال من أعلى إلى أسفل** </p><p>![ما يجب القيام به: image_بديل_نص](create-update-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**تخطيط الأشكال من اليسار إلى اليمين** </p><p>![ما يجب القيام به: image_بديل_نص](create-update-layout-and-auto-fit-shapes_4.png)</p>|<p>**تخطيط الأشكال من اليمين إلى اليسار** </p><p>![ما يجب القيام به: image_بديل_نص](create-update-layout-and-auto-fit-shapes_5.png)</p>|
لتخطيط الأشكال في نمط المخطط الانسيابي:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم بإنشاء مثيل لفئة LayoutOptions وقم بتعيين الخصائص ذات الصلة بنمط المخطط الانسيابي.
1. قم باستدعاء أسلوب تخطيط الفئة Diagram عن طريق تمرير LayoutOptions.
1. اتصل بـ Diagram class 'طريقة Save لكتابة رسم Visio.
### **عينة برمجة نمط المخطط الانسيابي**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-LayOutShapesInFlowchartStyle-LayOutShapesInFlowchartStyle.cs" >}}
### **تخطيط الأشكال في نمط الشجرة المضغوطة**
 يحاول نمط تخطيط الشجرة المضغوط بناء هيكل شجرة. يستخدم نفس ملف الإدخال مثل ملف[المثال أعلاه](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/)ويحفظ في العديد من أنماط الأشجار المدمجة المختلفة.

|<p>**تخطيط شجرة مضغوط - لأسفل ولليمين** </p><p>![ما يجب القيام به: image_بديل_نص](create-update-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**تخطيط شجرة مضغوط - لأسفل ولليسار** </p><p>![ما يجب القيام به: image_بديل_نص](create-update-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**تخطيط شجرة مضغوط - لليمين ولأسفل** </p><p>![ما يجب القيام به: image_بديل_نص](create-update-layout-and-auto-fit-shapes_8.png)</p>|<p>**تخطيط شجرة مضغوط - لليسار ولأسفل** </p><p>![ما يجب القيام به: image_بديل_نص](create-update-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
لتخطيط الأشكال في نمط الشجرة المدمجة:

1.  قم بإنشاء مثيل لـ[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) صف دراسي.
1. قم بإنشاء مثيل لفئة LayoutOptions وقم بتعيين خصائص نمط الشجرة المدمجة.
1. قم باستدعاء أسلوب تخطيط الفئة Diagram عن طريق تمرير LayoutOptions.
1. قم باستدعاء الأسلوب Save للفئة Diagram لكتابة ملف Visio.
#### **عينة برمجة نمط الشجرة المدمجة**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-LayOutShapesInCompactTreeStyle-LayOutShapesInCompactTreeStyle.cs" >}}
## **احتواء تلقائي Visio Diagram**
 Aspose.Diagram API يدعم التركيب التلقائي للرسم Visio. تساعد عملية الميزة هذه على إحضار الأشكال الخارجية داخل حدود الصفحة Visio. Aspose.Diagram for .NET API لديه[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) فئة تمثل رسم Visio. ال[مخطط حفظ الخيارات](https://reference.aspose.com/diagram/net/aspose.diagram.saving/diagramsaveoptions) تعرض الفئة خاصية AutoFitPageToDrawingContent لتلائم الرسم Visio تلقائيًا.

هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. قم بإنشاء كائن من فئة DiagramSaveOptions وتمرير تنسيق الملف الناتج.
1. قم بتعيين خاصية AutoFitPageToDrawingContent للكائن DiagramSaveOptions.
1. استدعاء طريقة حفظ لكائن الفئة Diagram وأيضا تمرير مسار الملف الكامل وكائن DiagramSaveOptions.
### **عينة البرمجة الملائمة التلقائية**
يوضح رمز المثال التالي كيفية احتواء الأشكال تلقائيًا في Visio diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-AutoFitShapesInVisio-AutoFitShapesInVisio.cs" >}}
## **العمل مع مشروع VBA**
### **تعديل كود وحدة VBA في Visio Diagram**
 توضح هذه المقالة كيفية تعديل رمز وحدة VBA تلقائيًا باستخدام Aspose.Diagram for .NET. لقد أضفنا[VbaModule](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModule), [مجموعة VbaModuleCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModuleCollection), [VbaProject](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProject), [VbaProjectReference](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReference) و[VbaProjectReferenceCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReferenceCollection) الطبقات. تساعد هذه الفئات في التحكم في مشروع VBA. يمكن للمطورين استخراج وتعديل رمز الوحدة النمطية لـ VBA.
### **تعديل نموذج برمجة رمز الوحدة النمطية لـ VBA**
الرجاء التحقق من مثال هذا الرمز:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-ModifyVBAModule-ModifyVBAModule.cs" >}}
### **قم بإزالة كافة وحدات الماكرو من Visio Diagram**
 Aspose.Diagram for .NET يسمح للمطورين بإزالة كافة وحدات الماكرو من Visio diagram.[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class ، تسمح لك بإزالة كافة وحدات الماكرو من الرسم Visio.
### **قم بإزالة كافة نماذج برمجة وحدات الماكرو**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RemoveMacrosFromVisio-RemoveMacrosFromVisio.cs" >}}
## **إنشاء Diagram جديد مع VSTO**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)يتيح للمطورين إنشاء مخططات Microsoft Office Visio والعمل معها ودمج الميزات في تطبيقات البرامج الخاصة بهم. هناك طرق أخرى للعمل مع Visio من الملفات ، والأكثر شيوعًا هو Microsoft Automation. لسوء الحظ ، هذا له بعض القيود. Aspose.Diagram قوي وسريع ويعمل بشكل مستقل دون تثبيت Microsoft Office.

 توضح مقالة الترحيل هذه كيفية الاستخدام أولاً[VSTO](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) وثم[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) لإنشاء diagram جديد وإضافة بعض الأشكال إليه. ستلاحظ أن كود Aspose.Diagram أقصر من كود VSTO. لا تتردد في استخدام الكود كأساس لتطويرك الخاص وتعزيزه لتلبية احتياجاتك. يتيح لك VSTO البرمجة باستخدام ملفات Microsoft Visio. لإنشاء diagram جديد:

1. قم بتكوين عنصر تطبيق Visio.
1. جعل كائن التطبيق غير مرئي.
1. قم بإنشاء diagram فارغًا.
1. أضف الأشكال من Visio الماجستير (الإستنسل).
1. احفظ الملف باسم VDX.
### **قم بإنشاء Diagram جديد باستخدام نموذج برمجة VSTO**
{{% alert color="primary" %}}

باستخدام Visio = Microsoft.Office.Interop.Visio ؛
الواردات Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}


**مثال:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-CreatingDiagramWithVSTO-CreatingDiagramWithVSTO.cs" >}}
## **إنشاء Diagram جديد مع Aspose.Diagram for .NET**
باستخدام Aspose.Diagram API ، لا يحتاج المطورون إلى تثبيت Microsoft Office Visio على الجهاز ، ويمكنهم العمل بشكل مستقل عن Microsoft Office Automation.

لإنشاء diagram جديد:

1. قم بإنشاء diagram فارغًا.
1. أضف الأشكال من Visio الماجستير (الإستنسل).
1. احفظ الملف باسم VDX.
### **Diagram جديد مع عينة برمجة Aspose.Diagram for .NET**
{{% alert color="primary" %}}

باستخدام Aspose.Diagram ؛
الواردات Aspose.Diagram

{{% /alert %}}

مثال:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-CreatingDiagramWithAspose-CreatingDiagramWithAspose.cs" >}}
## **تحديث خصائص الشكل**
 عند العمل باستخدام الرسوم التخطيطية Microsoft Visio ، يمكن للمستخدمين تحديث سمات الشكل بما في ذلك النص والنمط والموضع والارتفاع والعرض. بصفتك مطور برامج يعمل مع ملفات Visio ، سيُطلب منك القيام بذلك برمجيًا. والخبر السار هو أنه من الممكن ، إما باستخدام آليات البرمجة مع Visio الملفات التي يوفرها Microsoft أو VSTO أو باستخدام[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 يوضح الموضوع أدناه كيفية الاستخدام[VSTO](https://products.aspose.com/diagram/net/) و[Aspose.Diagram](https://products.aspose.com/diagram/net/) لتحديث خصائص الشكل. توضح مقتطفات التعليمات البرمجية أدناه كيفية تحديث خصائص الشكل لـ VSTO و Aspose.Diagram for .NET. لا تتردد في استخدام الكود وتطبيقه على حالتك الخاصة.
### **تحديث خصائص الشكل باستخدام VSTO**
يتيح لك VSTO البرمجة باستخدام ملفات Microsoft Visio. لتحديث خصائص الشكل:

1. قم بتكوين عنصر تطبيق Visio.
1. جعل كائن التطبيق غير مرئي.
1. افتح ملف Visio VSD موجود.
1. ابحث عن الشكل المطلوب.
1. قم بتحديث خصائص الشكل (النص ونمط النص والموضع والحجم).
1. احفظ الملف باسم VDX.
#### **تحديث خصائص الشكل بنموذج برمجة VSTO**
{{% alert color="primary" %}}

باستخدام Visio = Microsoft.Office.Interop.Visio ؛
الواردات Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}

**مثال:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-UpdateShapePropsWithVSTO-UpdateShapePropsWithVSTO.cs" >}}
### **تحديث خصائص الشكل مع Aspose.Diagram for .NET**
باستخدام Aspose.Diagram API ، لا يحتاج المطورون إلى Microsoft Office Visio على الجهاز ، ويمكنهم العمل بشكل مستقل عن Microsoft Office Automation.

لتحديث خصائص الشكل باستخدام Aspose.Diagram for .NET:

1. افتح ملف Visio VSD موجود.
1. ابحث عن الشكل المطلوب.
1. قم بتحديث خصائص الشكل (النص ونمط النص والموضع والحجم).
1. احفظ الملف باسم VDX.
#### **تحديث خصائص الشكل باستخدام عينة البرمجة Aspose.Diagram for .NET**
{{% alert color="primary" %}}

باستخدام Aspose.Diagram ؛
الواردات Aspose.Diagram

{{% /alert %}}

**مثال:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-UpdateShapePropsWithAspose-UpdateShapePropsWithAspose.cs" >}}
