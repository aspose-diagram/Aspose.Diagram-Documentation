---
title:  تحويل Visio إلى PDF تنسيق
linktitle: حوّل Visio إلى PDF
type: docs
weight: 10
url: /ar/net/convert-visio-to-pdf/
description: يوضح لك هذا الموضوع كيفية السماح Aspose.Diagram بتحويل تنسيق Visio إلى PDF. تحويل VSD، VSS، VDW، VST، VSDX، VSSX، VSTX، VSDM، VSTM،VSSM إلى PDF مع بضعة أسطر من التعليمات البرمجية.
---
## **تصدير إلى PDF**
{{% alert color="primary" %}}

 Aspose.Diagram for .NET يكتب مباشرة المعلومات حول API ورقم الإصدار في وثائق المخرجات. على سبيل المثال ، عند تقديم رسم إلى PDF ، يتم تعبئة Aspose.Diagram for .NET**طلب** حقل بقيمة "Aspose.Diagram" و**PDF منتج** حقل ذو قيمة ، على سبيل المثال "Aspose.Diagram 17.9".

يرجى ملاحظة أنه لا يمكنك توجيه Aspose.Diagram for .NET API لتغيير أو إزالة هذه المعلومات من مستندات الإخراج.

{{% /alert %}}

 يشرح هذا المقال كيفية تصدير Microsoft Visio diagram إلى PDF باستخدام[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

 استخدم ال[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) مُنشئ الفئة لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم.

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
توضح عينات الكود كيفية تصدير Microsoft Visio الرسم إلى PDF باستخدام C#.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-ExportToPDF-ExportToPDF.cs" >}}
### **تقسيم عدة صفحات**
Aspose.Diagram for .NET يسمح بتقسيم صفحات متعددة أثناء تحويل Microsoft Visio Diagram إلى PDF. يوضح مقتطف الكود التالي الوظيفة.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.cs" >}}
### **استخدم استدعاء حفظ الصفحة**
في حالة وجود صفحات متعددة ، يسمح Aspose.Diagram for .NET باستخدام رد اتصال حفظ الصفحة أثناء تحويل Microsoft Visio Diagram إلى PDF. يوضح مقتطف الشفرة التالي الوظيفة.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-PageSavingCallback.cs" >}}
#### **فئة TestDiagramPageSavingCallback**
{{< highlight "java" >}}

 اختبار الطبقة العامة

{  عام باطل PageStartSaving (Aspose.Diagram.Saving.PageStartSavingArgs args)   {  Console.WriteLine ("بدء حفظ صفحة diagram {0} من الصفحات {1}" argndPage، 1s.IPages. }   PageEndSaving عام باطل (Aspose.Diagram.Saving.PageEndSavingArgs args)   {  Console.WriteLine ("End save diagram page {0} argount of Pages {1}"، +   // لا تُخرج الصفحات بعد فهرس الصفحة 8.  if (args.PageIndex> = 8)   {  args.HasMorePages = false ؛  }  _x000_D_000 _x000
