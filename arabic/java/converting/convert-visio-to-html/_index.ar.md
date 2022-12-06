---
title:  تحويل Visio إلى تنسيق HTML
linktitle: تحويل Visio إلى HTML
type: docs
weight: 30
url: /ar/java/convert-visio-to-html/
description: يوضح لك هذا الموضوع كيفية السماح Aspose.Diagram بتحويل Visio إلى تنسيقات html. حول VSD، VSS، VDW، VST، VSDX، VSSX، VSTX، VSDM، VSTM،VSSM إلى html ببضعة سطور من التعليمات البرمجية.
---
## **تصدير Visio إلى HTML** **تصدير Visio إلى HTML**
 تشرح هذه المقالة كيفية تصدير Microsoft Visio diagram إلى HTML باستخدام[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 استخدم ال[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) مُنشئ الفئة لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم. يمكن للمطورين حفظ HTML الناتج في التخزين المحلي أو مباشرة في مثيل دفق.

1. [حفظ HTML الناتج في التخزين المحلي](/diagram/ar/java/how-to-convert-a-visio-diagram/).
1. [حفظ HTML الناتج في مثيل دفق](/diagram/ar/java/how-to-convert-a-visio-diagram/).

تُظهر الصورة أدناه ملف VSD حول ليتم حفظه بتنسيق PNG. يمكنك استخدام تنسيقات diagram أخرى (VSDX ، VSTM ، VSTM ، VSSX ، VSS ، VSSM ، VDX ، VST ، VSTX ، VDX ، VTX أو VSX) أيضًا.

**المدخلات diagram.**

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/YX4BNNq.png)

لتصدير VSD diagram إلى HTML ، قم بتنفيذ الخطوات التالية:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم باستدعاء فئة Dagram "Save method" وقم بتعيين HTML كتنسيق الإخراج.

توضح الصورة أدناه ملف HTML الناتج.

**إخراج HTML diagram.**

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/syavUqI.png)
### **حفظ HTML الناتج في التخزين المحلي**
يمكن حفظ الملف الناتج عن طريق تمرير سلسلة مسار كاملة ، بما في ذلك اسم الملف والملحق ، على سبيل المثال @ "c: \ temp \ MyOutput.html".
#### **حفظ HTML الناتج في نموذج برمجة التخزين المحلي**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToHTML-ExportToHTML.java" >}}



### **حفظ HTML الناتج في مثيل دفق**
إنها لحالة الاستخدام لحفظ HTML الناتج في قاعدة بيانات أو مستودع دون تخزينه في التخزين المحلي. تتضمن هذه الميزة أيضًا موارد ناتجة أخرى لـ HTML ، مثل الخطوط و CSS (التي تحتوي على معلومات النمط) والصور. نظرًا لأنه يحفظ ملف HTML واحدًا في مثيل الدفق.
#### **حفظ HTML الناتج في عينة برمجة دفق**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportHTMLinStream-ExportHTMLinStream.java" >}}
