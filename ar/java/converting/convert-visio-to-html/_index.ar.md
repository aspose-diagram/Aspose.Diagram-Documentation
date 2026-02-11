---
title:  تحويل Visio إلى HTML تنسيق
linktitle: حوّل Visio إلى HTML
type: docs
weight: 30
url: /ar/java/convert-visio-to-html/
description: يوضح لك هذا الموضوع كيفية السماح Aspose.Diagram بتحويل Visio إلى تنسيقات html. حول VSD، VSS، VDW، VST، VSDX، VSSX، VSTX، VSDM، VSTM،VSSM إلى html ببضع سطور من التعليمات البرمجية.
---
## **تصدير Visio إلى HTML** **تصدير Visio إلى HTML**
 يشرح هذا المقال كيفية تصدير Microsoft Visio diagram إلى HTML باستخدام[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 استخدم ال[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) مُنشئ الفئة لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم. يمكن للمطورين حفظ HTML الناتج في التخزين المحلي أو مباشرة في طبعة دفق.

1. [احفظ الناتج HTML في التخزين المحلي](/diagram/ar/java/how-to-convert-a-visio-diagram/).
1. [احفظ HTML الناتج في نسخة دفق](/diagram/ar/java/how-to-convert-a-visio-diagram/).

تُظهر الصورة أدناه ملف VSD على وشك حفظه بتنسيق PNG. يمكنك استخدام تنسيقات diagram أخرى (VSDX ، VSTM ، VSTM ، VSSX ، VSS ، VSSM ، VDX ، VST ، VSTX ، VDX ، VTX أو VSX) أيضًا.

**المدخلات diagram.**

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/YX4BNNq.png)

لتصدير VSD diagram إلى HTML ، قم بتنفيذ الخطوات التالية:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم باستدعاء فئة Dagram 'Save method وقم بتعيين HTML كتنسيق الإخراج.

توضح الصورة أدناه ملف الإخراج HTML.

**الخرج HTML diagram.**

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/syavUqI.png)
### **احفظ الناتج HTML في التخزين المحلي**
يمكن حفظ الملف الناتج عن طريق تمرير سلسلة مسار كاملة ، بما في ذلك اسم الملف والملحق ، على سبيل المثال @ "c: \ temp \ MyOutput.html".
#### **احفظ الناتج HTML في نموذج برمجة التخزين المحلي**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportToHTML.class);

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToHTML.vsd");

// Save as HTML
diagram.save(dataDir + "ExportToHTML_Out.html", SaveFileFormat.HTML);

{{< /highlight >}}
```



### **احفظ HTML الناتج في نسخة دفق**
يستخدم لحالة حفظ HTML الناتج في قاعدة بيانات أو مستودع دون تخزينه في التخزين المحلي. تتضمن هذه الميزة أيضًا الموارد الناتجة الأخرى لـ HTML ، مثل الخطوط و CSS (التي تحتوي على معلومات النمط) والصور. نظرًا لأنه يحفظ ملف HTML واحدًا في مثيل الدفق.
#### **حفظ HTML الناتج في عينة برمجة دفق**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportHTMLinStream.class);
// load diagram
Diagram diagram = new Diagram(dataDir + "ExportToHTML.vsd");
// save resultant HTML directly to a stream
ByteArrayOutputStream dstStream = new ByteArrayOutputStream();
diagram.save(dstStream, SaveFileFormat.HTML);
// In you want to read the result into a Diagram object again, in Java you need to get the
// data bytes and wrap into an input stream.
ByteArrayInputStream srcStream = new ByteArrayInputStream(dstStream.toByteArray());

{{< /highlight >}}
```
