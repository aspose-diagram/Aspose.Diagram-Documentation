---
title:  تحويل Visio إلى تنسيق HTML
linktitle: تحويل Visio إلى HTML
type: docs
weight: 30
url: /ar/python-net/convert-visio-to-html/
description: يوضح لك هذا الموضوع كيفية السماح Aspose.Diagram بتحويل Visio إلى تنسيقات html. حول VSD، VSS، VDW، VST، VSDX، VSSX، VSTX، VSDM، VSTM،VSSM إلى html ببضعة سطور من التعليمات البرمجية.
---
## **تصدير Visio إلى HTML**
 تشرح هذه المقالة كيفية تصدير Microsoft Visio diagram إلى HTML باستخدام[Aspose.Diagram لـ Python عبر .NET](https://products.aspose.com/diagram/python-net/) API.

استخدم مُنشئ الفئة Diagram لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم. يمكن للمطورين حفظ HTML الناتج في التخزين المحلي أو مباشرة في مثيل دفق.

1. [حفظ HTML الناتج في التخزين المحلي](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-the-local-storage).
1. [حفظ HTML الناتج في مثيل دفق](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-a-stream-instance).

تُظهر الصورة أدناه ملف VSD حول ليتم حفظه بتنسيق PNG. يمكنك استخدام تنسيقات diagram أخرى (VSDX ، VSDM ، VSTX ، VSSX ، VSS ، VSSM ، VDX ، VST ، VSTX ، VDX ، VTX أو VSX) أيضًا.

|**المدخلات diagram.**|
|:- |
|![ما يجب القيام به: image_بديل_نص](how-to-convert-a-visio-diagram_6.png)|
لتصدير VSD diagram إلى HTML ، قم بتنفيذ الخطوات التالية:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم باستدعاء فئة Dagram "Save method" وقم بتعيين HTML كتنسيق الإخراج.
### **حفظ HTML الناتج في التخزين المحلي**
يمكن حفظ الملف الناتج عن طريق تمرير سلسلة مسار كاملة ، بما في ذلك اسم الملف والملحق ، على سبيل المثال @ "c: \ temp \ MyOutput.html".
#### **حفظ HTML الناتج في نموذج برمجة التخزين المحلي**
{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToHTML.py" >}}
