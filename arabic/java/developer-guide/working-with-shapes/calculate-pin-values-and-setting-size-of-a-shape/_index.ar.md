---
title: حساب قيم الدبوس وتحديد حجم الشكل
type: docs
weight: 40
url: /ar/java/calculate-pin-values-and-setting-size-of-a-shape/
---
## **حساب قيم PinX و PinY للشكل الفرعي**
 إذا كان الشكل تابعًا لشكل مجموعة ، فإن xform هو إحداثي نسبي لشكله الأصل ， ولكن ليس إحداثيات مطلقة في[صفحة](https://reference.aspose.com/diagram/java/com.aspose.diagram/page). إذا طلب المستخدم الحصول على الإحداثيات المطلقة ، فإن نموذج التعليمات البرمجية هذا يساعد.

يمكن تحويل نقطة محددة في الإحداثيات المحلية إلى إحداثيات رئيسية من خلال تطبيق التحويلات التالية بالترتيب التالي:

1. اطرح قيمة الخاصية LocPinX لعنصر Cell_Type من إحداثي x.
1. اطرح قيمة الخاصية LocPinY الخاصة بنوع الخلية من الإحداثي ص.
1. قم بعكس النقطة حول المحور y إذا كانت قيمة خاصية FlipX في Cell_Type تساوي واحدًا.
1. عكس النقطة حول المحور x إذا كانت قيمة الخاصية FlipY في Cell_Type تساوي واحدًا.
1. قم بتدوير النقطة عكس اتجاه عقارب الساعة حول الأصل بقيمة خاصية Angle الخاصة بالنوع Cell_Type.
1. أضف قيمة PinX Cell_Type إلى إحداثيات x.
1. أضف قيمة PinY Cell_Type إلى الإحداثي y.
### **حساب عينة برمجة PinX و PinY**
استخدم الكود التالي في تطبيق Java لحساب قيم PinX و PinY لشكل فرعي باستخدام Aspose.Diagram for Java API.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-CalculateCenterOfSubShapes-CalculateCenterOfSubShapes.java" >}}
## **ضبط ارتفاع الشكل وعرضه**
 ال[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) تسمح لك الفئة بالتحكم في حجم الشكل عن طريق تحديد ارتفاع الشكل وعرضه باستخدام أساليب SetHeight و SetWidth.

 أساليب SetHeight و SetWidth ، المكشوفة بواسطة[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape)فئة ، دعم تغيير حجم الشكل مع السيد ، بدون الرئيسي أو في شكل شكل مجموعة.

تعيين أمثلة التعليمات البرمجية في هذه المقالة الارتفاع والعرض لتغيير حجم الشكل على الصفحة.

**المدخلات diagram** 

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/cTiNWa7.png)

**تم تغيير diagram بعد الارتفاع والعرض**

![ما يجب القيام به: image_بديل_نص](calculate-pin-values-and-setting-size-of-a-shape_1.png)

عملية ضبط الارتفاع والعرض هي:

1. قم بتحميل diagram.
1. ابحث عن شكل معين.
1. اضبط ارتفاع الشكل.
1. تعيين عرض الشكل.
1. احفظ diagram.
### **تعيين الارتفاع والعرض عينة البرمجة**
يوضح مقتطف الشفرة أدناه كيفية تعيين ارتفاع الشكل وعرضه. يبحث الكود عن مستطيل لاسم الشكل ، بمعرف الشكل 1 ، ويضبط الارتفاع والعرض على أنهما مزدوجان.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ChangeShapeSize-ChangeShapeSize.java" >}}
