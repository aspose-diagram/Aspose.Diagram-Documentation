---
title:  تحويل Visio إلى HTML تنسيق
linktitle: حوّل Visio إلى HTML
type: docs
weight: 30
url: /ar/python-java/convert-visio-to-html/
description: يوضح لك هذا الموضوع كيفية تحويل Visio إلى تنسيقات html باستخدام Aspose.Diagram لـ Python via Java. قم بتحويل VSD، VSS، VDW، VST، VSDX، VSSX، VSTX، VSDM، Aspose.Diagram برمز قليل.
---
## **تصدير Visio إلى HTML** ##
 يشرح هذا المقال كيفية تصدير Microsoft Visio diagram إلى HTML باستخدام[Aspose.Diagram لـ Python via Java](https://products.aspose.com/diagram/python-java/) API.

استخدم مُنشئ الفئة Diagram لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم. يمكن للمطورين حفظ HTML الناتج في التخزين المحلي أو مباشرة في طبعة دفق.

 الصورة أدناه تظهر أ[VSD ملف](ExportToHTML.vsd)على وشك أن يتم حفظها بتنسيق PNG. يمكنك استخدام تنسيقات diagram أخرى (VSDX ، VSTM ، VSTM ، VSSX ، VSS ، VSSM ، VDX ، VST ، VSTX ، VDX ، VTX أو VSX) أيضًا.

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

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# call the diagram constructor to load diagram from a VSD file
diagram = Diagram("ExportToHTML.vsd")

# Save as HTML
diagram.save("ExportToHTML_Out.html", SaveFileFormat.HTML)

jpype.shutdownJVM()

{{< /highlight >}}




### **احفظ HTML الناتج في نسخة دفق**
يستخدم لحالة حفظ HTML الناتج في قاعدة بيانات أو مستودع دون تخزينه في التخزين المحلي. تتضمن هذه الميزة أيضًا الموارد الناتجة الأخرى لـ HTML ، مثل الخطوط و CSS (التي تحتوي على معلومات النمط) والصور. نظرًا لأنه يحفظ ملف HTML واحدًا في مثيل الدفق.
#### **حفظ HTML الناتج في عينة برمجة دفق**

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load diagram
diagram = Diagram("ExportToHTML.vsd")
# save resultant HTML directly to a stream
dstStream = java.io.ByteArrayOutputStream()
diagram.save(dstStream, SaveFileFormat.HTML)
# In you want to read the result into a Diagram object again, you need to get the
# data bytes and wrap into an input stream.
# srcStream = java.io.ByteArrayInputStream(dstStream.toByteArray())

jpype.shutdownJVM()

{{< /highlight >}}

