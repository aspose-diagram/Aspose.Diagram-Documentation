---
title:  تحويل Visio إلى تنسيق PDF
linktitle: تحويل Visio إلى PDF
type: docs
weight: 10
url: /ar/python-java/convert-visio-to-pdf/
description: يوضح لك هذا الموضوع كيفية تحويل Visio إلى تنسيقات PDF باستخدام Aspose.Diagram لـ Python عبر Java. قم بتحويل VSD، VSS، VDW، VST، VSDX، VSSX، VSTX، VSDM، VSTM، VSSM برمز قليل.
---
## **التصدير إلى PDF**
{{% alert color="primary" %}}

يقوم Aspose.Diagram لـ Python عبر Java بكتابة المعلومات حول API ورقم الإصدار مباشرةً في مستندات الإخراج. على سبيل المثال ، عند تحويل رسم إلى PDF ، يتم تعبئة Aspose.Diagram for Java**طلب**حقل بقيمة "Aspose.Diagram" و**منتج PDF**حقل بقيمة ، على سبيل المثال "Aspose.Diagram 17.9".

يرجى ملاحظة أنه لا يمكنك توجيه Aspose.Diagram لـ Python عبر Java لتغيير أو إزالة هذه المعلومات من مستندات الإخراج.

{{% /alert %}}

يشرح هذا المقال كيفية تصدير Microsoft Visio diagram إلى PDF باستخدام Aspose.Diagram لـ Python عبر Java.

استخدم مُنشئ الفئة Diagram لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم.

[VSD diagram](ExportToPDF.vsd) هو مثال ملف الرسم لتصدير PDF. يمكنك استخدام تنسيقات diagram أخرى (VSS ، VSSX ، VSSM ، VDX ، VST ، VSTX ، VSTM ، VDX ، VTX أو VSX) أيضًا.

لتصدير VSD diagram إلى PDF:

1. قم بتكوين نسخة من الفئة Diagram.
1. اتصل على Diagram classs Save method واضبط تنسيق الإخراج على PDF.

### **تصدير إلى نموذج برمجة PDF**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToPDF.py" >}}

### **تقسيم عدة صفحات**
Aspose.Diagram for Java يسمح بتقسيم صفحات متعددة أثناء تحويل Microsoft Visio Diagram إلى PDF. يوضح مقتطف الشفرة التالي الوظيفة.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.py" >}}
