---
title:  تحويل Visio إلى PDF تنسيق
linktitle: حوّل Visio إلى PDF
type: docs
weight: 10
url: /ar/python-net/convert-visio-to-pdf/
description: يوضح لك هذا الموضوع كيفية السماح Aspose.Diagram بتحويل تنسيق Visio إلى PDF. تحويل VSD، VSS، VDW، VST، VSDX، VSSX، VSTX، VSDM، VSTM،VSSM إلى PDF مع بضعة أسطر من التعليمات البرمجية.
---
## **تصدير إلى PDF**
{{% alert color="primary" %}}

 يقوم Aspose.Diagram لـ Python via .NET بكتابة المعلومات حول API ورقم الإصدار مباشرةً في مستندات الإخراج. على سبيل المثال ، عند تقديم رسم إلى PDF ، يتم تعبئة Aspose.Diagram for .NET**طلب** حقل بقيمة "Aspose.Diagram" و**PDF منتج** حقل ذو قيمة ، على سبيل المثال "Aspose.Diagram 17.9".

يرجى ملاحظة أنه لا يمكنك توجيه Aspose.Diagram for .NET API لتغيير أو إزالة هذه المعلومات من مستندات الإخراج.

{{% /alert %}}

 يشرح هذا المقال كيفية تصدير Microsoft Visio diagram إلى PDF باستخدام[Aspose.Diagram لـ Python via .NET](https://products.aspose.com/diagram/python-net/) API.

استخدم مُنشئ الفئة [Diagram] لقراءة ملفات diagram وطريقة الحفظ لتصدير diagram إلى أي تنسيق صورة مدعوم.

توضح الصورة أدناه VSD diagram أن مقتطفات الشفرة أدناه تصدير PDF. يمكنك استخدام تنسيقات diagram أخرى (VSS ، VSSM ، VDX ، VST ، VSTX ، VDX ، VTX أو VSX) أيضًا.

|**الملف المصدر.**|
|:- |
|![ما يجب القيام به: image_بديل_نص](how-to-convert-a-visio-diagram_1.png)|


لتصدير VSD diagram إلى PDF:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم باستدعاء Diagram classs Save method واضبط تنسيق الإخراج على PDF.

يوجد أدناه صورة لملف الإخراج PDF.

|**ملف الإخراج PDF.**|
|:- |
|![ما يجب القيام به: image_بديل_نص](how-to-convert-a-visio-diagram_2.png)|
### **تصدير Microsoft Visio رسم إلى PDF**
توضح عينات الكود كيفية تصدير Microsoft Visio الرسم إلى PDF باستخدام Python.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToPdf.py" >}}
