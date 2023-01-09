---
title:  تحويل Visio إلى تنسيق PDF
linktitle: تحويل Visio إلى PDF
type: docs
weight: 10
url: /ar/java/convert-visio-to-pdf/
description: يوضح لك هذا الموضوع كيفية السماح Aspose.Diagram بتحويل Visio إلى تنسيقات PDF. قم بتحويل VSD، VSS، VDW، VST، VSDX، VSSX، VSTX، VSDM، VSTM،VSSM إلى PDF ببضعة سطور من التعليمات البرمجية.
---
## **التصدير إلى PDF**
{{% alert color="primary" %}}

Aspose.Diagram for Java يكتب مباشرة المعلومات حول API ورقم الإصدار في وثائق المخرجات. على سبيل المثال ، عند تحويل رسم إلى PDF ، يتم تعبئة Aspose.Diagram for Java**طلب**حقل بقيمة "Aspose.Diagram" و**منتج PDF**حقل بقيمة ، على سبيل المثال "Aspose.Diagram 17.9".

يرجى ملاحظة أنه لا يمكنك توجيه Aspose.Diagram for Java API لتغيير أو إزالة هذه المعلومات من مستندات الإخراج.

{{% /alert %}}

 يشرح هذا المقال كيفية تصدير Microsoft Visio diagram إلى PDF باستخدام[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 استخدم ال[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) مُنشئ class لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم.

توضح الصورة أدناه VSD diagram أن قصاصات التعليمات البرمجية الموجودة أسفل تصدير PDF. يمكنك استخدام تنسيقات diagram أخرى (VSS ، VSSX ، VSSM ، VDX ، VST ، VSTX ، VSTM ، VDX ، VTX أو VSX) أيضًا.

**الملف المصدر.**

![ما يجب القيام به: image_بديل_نص](how-to-convert-a-visio-diagram_1.png)

لتصدير VSD diagram إلى PDF:

1. قم بتكوين نسخة من الفئة Diagram.
1. اتصل على Diagram classs Save method واضبط تنسيق الإخراج على PDF.

يوجد أدناه صورة لملف PDF الناتج.

**ملف PDF الناتج.**

![ما يجب القيام به: image_بديل_نص](how-to-convert-a-visio-diagram_2.png)
### **تصدير إلى نموذج برمجة PDF**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToPDF-ExportToPDF.java" >}}
### **تقسيم عدة صفحات**
Aspose.Diagram for Java يسمح بتقسيم صفحات متعددة أثناء تحويل Microsoft Visio Diagram إلى PDF. يوضح مقتطف الشفرة التالي الوظيفة.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.java" >}}
### **استخدم استدعاء حفظ الصفحة**
في حالة وجود صفحات متعددة ، يسمح Aspose.Diagram for Java باستخدام خاصية استعادة الصفحة أثناء تحويل Microsoft Visio Diagram إلى PDF. يوضح مقتطف الشفرة التالي الوظيفة.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-DiagramConversions-DocumentConversionProgress-1.java" >}}

#### **فئة TestDiagramPageSavingCallback**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-DiagramConversions-DocumentConversionProgress-2.java" >}}
