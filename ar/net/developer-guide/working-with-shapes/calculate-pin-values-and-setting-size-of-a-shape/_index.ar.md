---
title: حساب قيم الدبوس وتحديد حجم الشكل
type: docs
weight: 60
url: /ar/net/calculate-pin-values-and-setting-size-of-a-shape/
description: يشرح هذا القسم كيفية حساب قيم PinX و PinY للشكل الفرعي مع Aspose.Diagram.
---
## **حساب قيم PinX و PinY للشكل الفرعي**
 إذا كان الشكل عبارة عن عقدة فرعية لشكل المجموعة ، فإن xform الخاص به هو إحداثي نسبي لشكله الأصلي ولكنه ليس تنسيقًا مطلقًا في[صفحة](http://www.aspose.com/api/net/diagram/aspose.diagram/page). إذا طلب المستخدم الحصول على الإحداثيات المطلقة ، فإن نموذج التعليمات البرمجية هذا يساعد.

يمكن تحويل نقطة محددة في الإحداثيات المحلية إلى إحداثيات رئيسية من خلال تطبيق التحويلات التالية بالترتيب التالي:

1. اطرح قيمة الخاصية LocPinX لعنصر Cell_Type من إحداثي x.
1. اطرح قيمة الخاصية LocPinY الخاصة بنوع الخلية من الإحداثي ص.
1. قم بعكس النقطة حول المحور y إذا كانت قيمة خاصية FlipX في Cell_Type تساوي واحدًا.
1. عكس النقطة حول المحور x إذا كانت قيمة الخاصية FlipY في Cell_Type تساوي واحدًا.
1. قم بتدوير النقطة عكس اتجاه عقارب الساعة حول الأصل بقيمة خاصية Angle الخاصة بالنوع Cell_Type.
1. أضف قيمة PinX Cell_Type إلى إحداثيات x.
1. أضف قيمة PinY Cell_Type إلى الإحداثي y.
### **حساب عينة برمجة PinX و PinY**
استخدم الكود التالي في تطبيق .NET لحساب قيم PinX و PinY لشكل فرعي باستخدام Aspose.Diagram for .NET API.







{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-CalculateCenterOfSubShapes-CalculateCenterOfSubShapes.cs" >}}
## **ضبط ارتفاع الشكل وعرضه**
 ال[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) تسمح لك الفئة بالتحكم في حجم الشكل عن طريق تحديد ارتفاع الشكل وعرضه باستخدام أساليب SetHeight و SetWidth.

 أساليب SetHeight و SetWidth ، المكشوفة بواسطة[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)فئة ، دعم تغيير حجم الشكل مع السيد ، بدون الرئيسي أو في شكل شكل مجموعة. تعيين أمثلة التعليمات البرمجية في هذه المقالة الارتفاع والعرض لتغيير حجم الشكل على الصفحة.

عملية ضبط الارتفاع والعرض هي:

1. قم بتحميل diagram.
1. ابحث عن شكل معين.
1. اضبط ارتفاع الشكل.
1. تعيين عرض الشكل.
1. احفظ diagram.
### **تعيين الارتفاع والعرض عينة البرمجة**
يوضح مقتطف الشفرة أدناه كيفية تعيين ارتفاع الشكل وعرضه. يبحث الكود عن مستطيل لاسم الشكل ، بمعرف الشكل 1 ، ويضبط الارتفاع والعرض على أنهما مزدوجان.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-ChangeShapeSize-ChangeShapeSize.cs" >}}
