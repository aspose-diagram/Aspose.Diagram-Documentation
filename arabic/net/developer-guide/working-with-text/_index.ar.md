---
title: العمل مع النص
type: docs
weight: 90
url: /ar/net/working-with-text/
description: يوضح هذا القسم كيفية إدراج شكل نص أو تحديث نص الشكل باستخدام Aspose.Diagram.
---
## **أدخل شكل نص في صفحة Visio**
 Aspose.Diagram API يتيح للمطورين إدراج شكل نص في أي مكان في صفحة Visio. لتحقيق ذلك ، فإن أسلوب AddText الخاص ببرنامج[صفحة](http://www.aspose.com/api/net/diagram/aspose.diagram/page) يأخذ الفصل معلمات PinX و PinY والعرض والارتفاع والنص.
### **أدخل نموذجًا لبرمجة شكل النص**
يضيف جزء الكود التالي شكل نص في Visio diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-InsertTextShape-InsertTextShape.cs" >}}
## **تحديث Visio شكل النص**
 إلى جانب[إنشاء الرسوم البيانية](/diagram/ar/net/load-or-create-a-visio-drawing/) ، Aspose.Diagram for .NET يتيح لك العمل مع الأشكال بطرق مختلفة. تتناول هذه المقالة كيفية الوصول إلى النص في الأشكال وتحديثه. خاصية Text ، المكشوفة بواسطة ملف[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) فئة ، تدعم الكائن Aspose.Diagram.Text. يمكن استخدام الخاصية لاسترداد نص الشكل أو تحديثه. عملية تحديث نص الشكل مباشرة:

1. قم بتحميل diagram.
1. ابحث عن شكل معين.
1. قم بتعيين النص الجديد.
1. احفظ diagram.
### **تحديث نموذج برمجة نص الشكل**
يقوم الجزء التالي من التعليمات البرمجية بتحديث نص الشكل. يتم تحديد الأشكال من خلال معرفاتهم. تبحث مقاطع التعليمات البرمجية أدناه عن شكل يسمى العملية ومع المعرف 1 وتغيير نصه.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-UpdateShapeText-UpdateShapeText.cs" >}}
## **قم بتطبيق ورقة أنماط مدمجة أو مخصصة على شكل Visio**
تخزن أوراق الأنماط Microsoft Visio معلومات التنسيق التي يمكن تطبيقها على الأشكال للحصول على مظهر وأسلوب عرض متسقين. Aspose.Diagram for .NET يسمح لك بتطبيق أوراق الأنماط من داخل التطبيق.

 خصائص TextStyle و FillStyle و LineStyle المعروضة بواسطة ملف[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) فئة دعم[Aspose.Diagram.StyleSheet](http://www.aspose.com/api/net/diagram/aspose.diagram/stylesheet) هدف. يمكن استخدام الخاصية لاسترداد معلومات النمط وتطبيق أنماط مخصصة للنص والخط والتعبئة على diagram.
### **الأنماط المخصصة في Microsoft Visio**
لتطبيق أنماط مخصصة على الأشكال في Microsoft Visio:

1. افتح diagram في Microsoft Visio.
1.  يختار**تحديد الأنماط** من**شكل** القائمة (Visio 2007) ، أو انقر بزر الماوس الأيمن**الأنماط** في ال**مستكشف الرسم** نافذة ، وحدد**تحديد الأنماط** (Visio 2010).
1.  في ال**تحديد الأنماط** في مربع الحوار ، اكتب اسمًا جديدًا لورقة الأنماط المخصصة الخاصة بك. على سبيل المثال ، CustomStyle1.
1.  انقر على**نص**, **خط** و**يملأ** لتعيين أنماط النص والخط والتعبئة على التوالي.
1.  انقر**نعم**.

بعد تحديد أوراق الأنماط المخصصة في Microsoft Visio ، استخدم الكود التالي في تطبيق .NET لتطبيق الأنماط المخصصة على الأشكال الخاصة بك. لاحظ أن نماذج التعليمات البرمجية أدناه تستدعي ورقة الأنماط المخصصة المحددة أعلاه: تحتاج إلى معرفة اسم وموقع الورقة التي تقوم بتطبيقها. لتطبيق الأنماط المخصصة برمجيًا:

1. قم بتحميل diagram.
1. ابحث عن الشكل الذي تريد تطبيق النمط عليه.
1. قم بتحميل ورقة الأنماط.
1. تطبيق الأنماط.
1. احفظ diagram.
#### **تطبيق نموذج برمجة أنماط مخصصة**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-ApplyCustomStyleSheets-ApplyCustomStyleSheets.cs" >}}
## **قم بتطبيق نمط مختلف على كل قيمة نصية لشكل**
 إلى جانب[إنشاء الرسوم البيانية](/diagram/ar/net/load-or-create-a-visio-drawing/)، Aspose.Diagram for .NET يتيح لك العمل مع الأشكال بطرق مختلفة. تساعد هذه المقالة في إضافة قيم نصية متعددة إلى شكل وتطبيق نمط مختلف على كل قيمة نصية.

{{% alert color="primary" %}} 

يحتوي عنصر الشكل على عنصر يسمى Text ، والذي يحتوي على أحرف النص والعناصر الخاصة (cp و pp و tp و fld) التي تحدد نهاية تشغيل واحد وبداية تشغيل التالي. يحتوي Char Element على سمات التنسيق لنص الشكل ، مثل الخط واللون ونمط النص والحالة والموقع بالنسبة إلى الخط الأساسي وحجم النقطة.

{{% /alert %}} 
### **إضافة نص الشكل والأنماط**

|**المدخلات diagram**|
|:- |
|![ما يجب القيام به: image_بديل_نص](working-with-text_1.png)|


|**Diagram بعد إضافة قيم نصية مختلفة لشكل بنمط مختلف لكل قيمة نصية**|
|:- |
|![ما يجب القيام به: image_بديل_نص](working-with-text_2.png)|
#### **إضافة نموذج برمجة نص وأنماط**
تضيف قطعة الكود التالية نصًا للشكل وأنماطًا مختلفة.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-ApplyFontOnText-ApplyFontOnText.cs" >}}
## **البحث عن نص الشكل واستبداله**
 ال[رسالة قصيرة](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) يسمح لك Class بتعديل نص الشكل. طريقة الاستبدال ، المكشوفة بواسطة[رسالة قصيرة](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) فئة ، دعم تغيير نص الشكل.
تبحث أمثلة التعليمات البرمجية في هذه المقالة عن نص الشكل على الصفحة واستبداله.

|**المدخلات diagram**|
|:- |
|![ما يجب القيام به: image_بديل_نص](working-with-text_3.png)|


|**diagram بعد تحرير الشكل**|
|:- |
|![ما يجب القيام به: image_بديل_نص](working-with-text_4.png)|
عملية تغيير نص الشكل:

1. قم بتحميل diagram.
1. ابحث عن نص معين للشكل.
1. استبدل نص هذا الشكل
1. احفظ diagram.
### **بحث واستبدال عينة برمجة نصية**
توضح مقتطفات التعليمات البرمجية أدناه كيفية تعديل نص الشكل. تتكرر الشفرة عبر أشكال الصفحة.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-FindAndReplaceShapeText-FindAndReplaceShapeText.cs" >}}
## **استخراج نص عادي من Visio Diagram صفحة**
Aspose.Diagram API يسمح للمطورين باستخراج نص عادي من صفحة Visio diagram. يمكنهم أيضًا تكرار الصفحات Visio diagram لتغطية النص Visio diagram بالكامل.

 Microsoft Office Visio يقوم باضافة النص الى الاشكال. ال[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) تحتوي الفئة على عنصر يسمى Text ، والذي يحتوي على أحرف النص والعناصر الخاصة (cp ، و pp ، و tp ، و fld) التي تحدد نهاية تشغيل واحد وبداية تشغيل ما يليه.
### **استخراج عينة برمجة نص عادي**
يتكرر جزء الكود التالي من خلال أشكال الصفحة Visio ويقوم بتصفية النص العادي بدون معلومات التنسيق.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-GetPlainTextOfVisio-GetPlainTextOfVisio.cs" >}}
