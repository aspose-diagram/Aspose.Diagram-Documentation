---
title:  تحويل Visio إلى HTML تنسيق
linktitle: حوّل Visio إلى HTML
type: docs
weight: 30
url: /ar/net/convert-visio-to-html/
description: يوضح لك هذا الموضوع كيفية السماح Aspose.Diagram بتحويل Visio إلى تنسيقات html. حول VSD، VSS، VDW، VST، VSDX، VSSX، VSTX، VSDM، VSTM،VSSM إلى html ببضع سطور من التعليمات البرمجية.
---
## **تصدير Visio إلى HTML**
 يشرح هذا المقال كيفية تصدير Microsoft Visio diagram إلى HTML باستخدام[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

 استخدم ال[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) مُنشئ الفئة لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم. يمكن للمطورين حفظ HTML الناتج في التخزين المحلي أو مباشرة في طبعة دفق.

1. [احفظ الناتج HTML في التخزين المحلي](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-the-local-storage).
1. [احفظ HTML الناتج في نسخة دفق](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-a-stream-instance).

تُظهر الصورة أدناه ملف VSD على وشك حفظه بتنسيق PNG. يمكنك استخدام تنسيقات diagram أخرى (VSDX ، VSDM ، VSTX ، VSSX ، VSS ، VSSM ، VDX ، VST ، VSTX ، VDX ، VTX أو VSX) أيضًا.

|**المدخلات diagram.**|
|:- |
|![ما يجب القيام به: image_بديل_نص](how-to-convert-a-visio-diagram_6.png)|
لتصدير VSD diagram إلى HTML ، قم بتنفيذ الخطوات التالية:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم باستدعاء فئة Dagram 'Save method وقم بتعيين HTML كتنسيق الإخراج.
### **احفظ الناتج HTML في التخزين المحلي**
يمكن حفظ الملف الناتج عن طريق تمرير سلسلة مسار كاملة ، بما في ذلك اسم الملف والملحق ، على سبيل المثال @ "c: \ temp \ MyOutput.html".
#### **احفظ الناتج HTML في نموذج برمجة التخزين المحلي**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
// Load diagram
Diagram diagram = new Diagram(dataDir + "ExportToHTML.vsd");
// Save diagram
diagram.Save(dataDir + "outputVSDtoHTML.html", SaveFileFormat.HTML);

{{< /highlight >}}
```



### **احفظ HTML الناتج في نسخة دفق**
يستخدم لحالة حفظ HTML الناتج في قاعدة بيانات أو مستودع دون تخزينه في التخزين المحلي. تتضمن هذه الميزة أيضًا الموارد الناتجة الأخرى لـ HTML ، مثل الخطوط و CSS (التي تحتوي على معلومات النمط) والصور. نظرًا لأنه يحفظ ملف HTML واحدًا في مثيل الدفق.
#### **حفظ HTML الناتج في عينة برمجة دفق**
{{< highlight "java" >}}

 // Load an existing visio diagram

Diagram diagram = new Diagram("Basic Flowchart.vsd");

// Save resultant HTML directly to a stream

MemoryStream stream = new MemoryStream();

diagram.Save(stream, SaveFileFormat.HTML);



{{< /highlight >}}
