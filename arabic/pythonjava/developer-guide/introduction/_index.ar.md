---
title: مقدمة
type: docs
weight: 10
url: /ar/net/introduction/
description: استحداث مكتبة Aspose.Diagram.
---
## **احصل على معلومات المستند Visio للمكتبة Aspose.Diagram for .NET**
Microsoft Visio يحفظ معلومات حول الإجراءات التي تم اتخاذها على diagram داخل الملف. على سبيل المثال ، يتم حفظ وقت وتاريخ إنشاء المستند ، وآخر مرة تم فيها تحريره أو طباعته أو حفظه ، مع الملف. يتم أيضًا حفظ المعلومات الخاصة بإصدار Microsoft Visio الذي تم إنشاؤه وإجراء آخر تحرير للملف.

تشرح هذه المقالة كيفية استرداد تلك المعلومات.
### **تحديد إصدار Microsoft Visio الذي تم إنشاؤه وتحريره وحفظه في مستند**
 تعرض خاصية الإصدار بواسطة ملف[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/)يتم استخدام الفئة وخاصية BuildNumberCreated المعروضة بواسطة فئة DocumentProperties لتحديد الإصدار ورقم البنية الكامل لمثيل Microsoft Visio المستخدم لإنشاء المستند.

 الخاصية BuildNumberEdited التي يعرضها[خصائص المستند](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties) يتم استخدام الفئة لتحديد رقم البنية الكامل لمثيل Microsoft Visio المستخدم لتحرير الوثيقة.

يتم استخدام خصائص TimeCreated و TimeEdited و TimePrinted و TimeSaved التي تعرضها فئة DocumentProperties لتحديد الوقت الذي تم فيه إنشاء المستند Microsoft Visio وآخر تحرير وطباعته وآخر مرة تم حفظه فيها.

يمكنك أيضًا تعيين هذه الخصائص لتغيير المعلومات الموجودة في الملف. توضح نماذج التعليمات البرمجية أدناه كيفية استرداد المعلومات حول ما تم إنشاء الملف وكذلك وقت إنشائه وتحريره وطباعته وحفظه.
#### **عينة البرمجة**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-GetLibraryVersion-GetLibraryVersion.cs" >}}
## **كتابة Visio معلومات ملخص المستند**
يتيح لك Microsoft Visio تحديد عدد من خصائص معلومات ملخص المستند لمساعدتك وزملاؤك في تحديد diagram. خصائص الملخص ، على سبيل المثال ، العنوان والموضوع والمؤلف والوصف ، مما يسهل العثور على الملف عند البحث ويسهل التعرف عليه عند تصفح الملفات.
### **كتابة Microsoft Visio معلومات ملخص المستند**
تعرض فئة DocumentProperties عددًا من الخصائص لتعيين معلومات تلخيصية Microsoft Microsoft diagram أو الحصول عليها. يمكن لـ Aspose.Diagram for .NET تحديث معلومات ملخص الرسم ثم إعادة كتابة ملف الرسم إلى VDX.

{{% alert color="primary" %}} 

يرجى ملاحظة أنه لا يمكنك تعيين القيم مقابل**طلب**و**منتج**الحقول ، لأنه سيتم عرض Aspose Ltd. و Aspose.Diagram for .NET xxx مقابل هذه الحقول.

{{% /alert %}} 

لتحديث معلومات ملخص الرسم لملف VDX أو VSD موجود:

1.  قم بإنشاء مثيل لـ[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/) صف دراسي.
1.  تعيين الخصائص المكشوفة بواسطة[Diagram.DocumentProps](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/properties/documentprops) لتعريف معلومات التلخيص لملف الرسم Visio.
1. قم باستدعاء الأسلوب Save للفئة Diagram لكتابة ملف الرسم Visio إلى VDX.

تحقق من المعلومات الموجزة:

1. افتح ملف الإخراج VDX في Microsoft Visio.
1. اختيار المعلومات من القائمة ملف.
#### **كتابة Visio نموذج برمجة معلومات ملخص الوثيقة**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-SetVisioProperties-SetVisioProperties.cs" >}}
## **كشف تنسيق ملف Visio**
باستخدام Aspose.Diagram for .NET API ، يمكن للمطورين اكتشاف تنسيق الملف Visio قبل فتحه لأن امتداد الملف لا يضمن أن محتوى الملف مناسب.
### **كشف نموذج برمجة التنسيق**
يوضح نموذج التعليمات البرمجية التالي كيفية اكتشاف تنسيق ملف (باستخدام مسار الملف أو دفقه) والتحقق من امتداده.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-DetectVisioFileFormat-DetectVisioFileFormat.cs" >}}
