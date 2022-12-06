---
title:  تحويل Visio إلى تنسيقات الصور
linktitle: تحويل Visio إلى صور
type: docs
weight: 20
url: /ar/java/convert-visio-to-image/
description: يوضح لك هذا الموضوع كيفية السماح Aspose.Diagram بتحويل Visio إلى تنسيقات صور مختلفة. تحويل Visio،VSD ، VSS ، VDW ، VST ، VSDX ، VSSX ، VSTX ، VSDM ، VSTM،VSSM إلى صور PNG ، JPEG ، BMP مع بضعة أسطر من التعليمات البرمجية.
---
## **تصدير المخططات إلى تنسيقات ملفات الصور**
 يشرح هذا المقال كيفية تصدير Microsoft Visio diagram إلى صورة باستخدام[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 استخدم ال[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)class 'منشئ لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم. تُظهر الصورة أدناه ملف VSD ليتم حفظه بتنسيق PNG. يمكنك استخدام تنسيقات diagram أخرى (VSS ، VSSX ، VSSM ، VDX ، VST ، VSTX ، VSTM ، VDX ، VTX أو VSX) أيضًا.
**الملف المصدر. لاحظ أن تسميات السهم والمثلث بخط غامق.**

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/WOV36ek.png)

لتصدير diagram إلى صورة:

- قم بتكوين نسخة من الفئة Diagram.
- اتصل بـ Diagram class 'Save method وقم بتعيين تنسيق الصورة الذي تريد التصدير إليه ، ملف صورة الإخراج يبدو مثل الملف الأصلي.

**ملف PNG الناتج.**

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/WOV36ek.png)
### **التصدير إلى نموذج برمجة ملفات الصور**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToImage-ExportToImage.java" >}}

من الممكن أيضًا حفظ صفحة معينة على الصورة ، بدلاً من حفظ المستند بأكمله:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportPageToImage-ExportPageToImage.java" >}}