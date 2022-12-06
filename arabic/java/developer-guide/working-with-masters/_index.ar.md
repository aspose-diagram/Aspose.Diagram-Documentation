---
title: العمل مع الماجستير
type: docs
weight: 30
url: /ar/java/working-with-masters/
---
## **استرجاع معلومات الماجستير**
سيد الشكل هو اسم آخر لاستنسل Visio. باستخدام Aspose.Diagram ، يمكن استرجاع معلومات حول الصفحات والموصلات وأيضًا الرئيسية. تشرح هذه المقالة كيفية الحصول على المعرف والاسم من diagram.

 ال[يتقن](https://reference.aspose.com/diagram/java/com.aspose.diagram/master) الكائن يمثل أ[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)كائن رئيسي في diagram. الخاصية الرئيسية ، التي تم الكشف عنها بواسطة الفئة Diagram ، تدعم مجموعة من Aspose.Diagram.Master الكائنات. يمكن استخدام هذه الخاصية لاسترداد المعلومات الرئيسية وهي المعرف الرئيسي والاسم.

استخدم خاصية Page.Shapes لتحديد الشكل الذي ورثه الشكل الرئيسي.

**نافذة وحدة التحكم تظهر الإخراج من الكود.** 

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/DPn5sP9.png)
### **استرجاع نموذج برمجة معلومات الماجستير**
يسترد جزء الكود التالي المعلومات الرئيسية من diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-RetrieveMasterInfo-RetrieveMasterInfo.java" >}}
## **أضف ماستر من استنسل الأشكال**
الاستنسل هو مجموعة من الأشكال المرتبطة بقالب Microsoft Office Visio معين. باستخدام Aspose.Diagram ، يمكن إضافة أي شكل رئيسي إلى رسم من استنسل.
### **إضافة ماجستير**
يمثل الكائن الرئيسي رئيسي كائن الشكل في diagram. تسمح طريقة AddMaster ، المكشوفة بواسطة فئة Diagram ، بإضافة رئيسي من استنسل. يقدم الطرق الأربع التالية:

- مسار ملف الاستنسل والمعرف الرئيسي.
- مسار ملف الاستنسل والاسم الرئيسي.
- دفق ملف الاستنسل والمعرف الرئيسي.
- دفق ملف الاستنسل والاسم الرئيسي.
- أضف رئيسي إلى diagram من المصدر diagram
#### **إضافة عينة البرمجة الرئيسية**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-AddMasterFromStencil-AddMasterFromStencil.java" >}}
## **إنشاء ماجستير من الصفر**
Aspose.Diagram API يسمح بإنشاء Master من البداية دون أي استنسل أو رسم أو قالب. يمكن للمطورين تخصيص إنشاء Master. تسمح طريقة addMaster ، التي تم الكشف عنها بواسطة فئة Diagram ، بإضافة عنصر رئيسي.
#### **إنشاء عينة البرمجة الرئيسية**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-CreateMasterfromScratch-CreateMasterfromScratch.java" >}}

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-BASE64Encoder-BASE64Encoder.java" >}}
## **احصل على درجة الماجستير من ملف Visio**
في بعض الأحيان ، يحتاج المطورون إلى الحصول على تفاصيل سيد رسم Visio. يدعم Aspose.Diagram API هذه الميزة.

 يقدم Aspose.Diagram for Java[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)فئة تمثل رسم Visio. تدعم الخاصية Masters ، المكشوفة بواسطة الفئة Diagram ، مجموعة من Aspose.Diagram.Master الكائنات. يمكن استخدام هذه الخاصية لاسترداد تفاصيل رئيسية معينة. تعرض فئة MasterCollection أساليب GetMasterByName و GetMaster التي يمكن استدعاؤها للحصول على كائن رئيسي.
### **الحصول على كائن رئيسي بواسطة المعرف**
هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. اتصل بـ Diagram.Masters class 'GetMaster method.
#### **كائن رئيسي عن طريق نموذج برمجة معرف**
يوضح المثال التالي كيفية الحصول على سيد بواسطة المعرف من رسم Visio.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-GetMasterbyID-GetMasterbyID.java" >}}
### **الحصول على كائن رئيسي بالاسم**
هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. استدعاء Diagram.Masters class 'أسلوب GetMasterByName.
#### **كائن رئيسي حسب عينة برمجة الاسم**
يوضح المثال التالي كيفية الحصول على كائن رئيسي بالاسم من رسم Visio.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-GetMasterbyName-GetMasterbyName.java" >}}
## **تحقق من وجود ماجستير في رسم Visio**
يدعم Aspose.Diagram API التحقق من وجود سيد في رسم Visio. باستخدام خاصية MasterCollection ، يمكن للمطورين التحقق لمعرفة ما إذا كان المعلم موجودًا بالاسم أو المعرف.

 يقدم Aspose.Diagram for Java[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) فئة تمثل رسم Visio. تدعم الخاصية Masters ، المكشوفة بواسطة الفئة Diagram ، مجموعة من Aspose.Diagram.Master الكائنات. يمكن استخدام هذه الخاصية للتحقق من وجود سيد معين. تعرض فئة MasterCollection طريقة IsExist التي يمكن استدعاؤها بالاسم الرئيسي أو معلمة المعرف.
### **التحقق من وجود رئيسي عن طريق المعرف**
هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. اتصل على Diagram.Masters class 'طريقة IsExist.
#### **حضور ماجستير عن طريق نموذج برمجة معرف**
يوضح المثال التالي كيفية التحقق من وجود رئيسي بواسطة المعرف في رسم Visio.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-CheckMasterPresencebyID-CheckMasterPresencebyID.java" >}}
### **التحقق من وجود رئيسي بالاسم**
هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. اتصل على Diagram.Masters class 'طريقة IsExist.
#### **حضور ماجستير من خلال نموذج برمجة الاسم**
يوضح المثال التالي كيفية التحقق من وجود رئيسي بالاسم من رسم Visio.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-CheckMasterPresencebyName-CheckMasterPresencebyName.java" >}}
