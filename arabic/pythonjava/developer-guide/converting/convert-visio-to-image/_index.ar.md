---
title:  تحويل Visio إلى تنسيقات الصور
linktitle: تحويل Visio إلى صور
type: docs
weight: 20
url: /ar/python-java/convert-visio-to-image/
description: يوضح لك هذا الموضوع كيفية تحويل Visio إلى تنسيقات صور متنوعة باستخدام Aspose.Diagram لـ Python عبر Java. قم بتحويل Visio،VSD ، VSS ، VDW ، VST ، VSDX ، VSSX ، VSTX ، VSDM ، 076110 JP3481 ، إلى 076110 JP3481 بضعة أسطر من التعليمات البرمجية.
---
## **تصدير المخططات إلى تنسيقات ملفات الصور**
يشرح هذا المقال كيفية تصدير Microsoft Visio diagram إلى صورة باستخدام Aspose.Diagram لـ Python عبر Java.

استخدم مُنشئ الفئة Diagram لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم. تُظهر الصورة أدناه ملف VSD ليتم حفظه بتنسيق PNG. يمكنك استخدام تنسيقات diagram أخرى (VSS ، VSSX ، VSSM ، VDX ، VST ، VSTX ، VSTM ، VDX ، VTX أو VSX) أيضًا.

**[على سبيل المثال ملف VSD.] (ExportToImage.vsd)**

لتصدير diagram إلى صورة:

- قم بتكوين نسخة من الفئة Diagram.
- اتصل بـ Diagram class 'Save method وقم بتعيين تنسيق الصورة الذي تريد التصدير إليه ، ملف صورة الإخراج يبدو مثل الملف الأصلي.

**ملف PNG الناتج.**

![ما يجب القيام به: image_بديل_نص](ExportToImage.png)
### **التصدير إلى نموذج برمجة ملفات الصور**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToImage.py" >}}

من الممكن أيضًا حفظ صفحة معينة على الصورة ، بدلاً من حفظ المستند بأكمله:

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportPageToImage.py" >}}