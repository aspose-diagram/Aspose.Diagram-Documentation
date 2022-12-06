---
title:  قم بتحويل Visio إلى تنسيقات أخرى
linktitle:  قم بتحويل Visio إلى تنسيقات أخرى
type: docs
weight: 40
url: /ar/python-java/convert-visio-to-other-files/
description: يوضح لك هذا الموضوع كيفية تحويل Visio إلى تنسيقات SVG و XPS و XML و XAML باستخدام Aspose.Diagram لـ Python عبر Java. ، XAML مع بضعة أسطر من التعليمات البرمجية.
---
**[للتصدير Microsoft Visio diagram.] (ExportToXML.vsd)**

## **التصدير إلى XML**
تشرح هذه المقالة كيفية تصدير Microsoft Visio diagram إلى XML باستخدام Aspose.Diagram لـ Python عبر Java.

- يعرف VDX XML diagram.
- يقوم VTX بتعريف قالب XML.
- يعرف VSX استنسل XML.

تقرأ مُنشئات الفئة Diagram diagram وتستخدم طريقة الحفظ لحفظ أو تصدير diagram بتنسيق ملف مختلف. توضح مقتطفات التعليمات البرمجية في هذه المقالة كيفية استخدام طريقة الحفظ لحفظ ملف Visio بتنسيقات VDX و VTX و VSX.

### **تصدير VSD الى VDX**
VDX هو تنسيق ملف XML مستند إلى مخطط يسمح لك بحفظ الرسوم التخطيطية بتنسيق يمكن أن تقرأه منتجات بخلاف Microsoft Visio. إنه تنسيق مفيد لنقل المخططات بين تطبيقات البرامج والاحتفاظ بالبيانات القابلة للتحرير.

لتصدير VSD diagram إلى VDX:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم باستدعاء الأسلوب Save للفئة Diagram لكتابة ملف الرسم Visio إلى VDX.

### **تصدير من VSD الى VSX**
VSX هو نسق XML لتعريف الإستنسل ، الكائنات الأساسية التي تم بناء diagram منها. عند تحويل ملف Visio إلى VSX ، يتم تصدير قوالب الإستنسل فقط.

لتصدير VSD diagram إلى VSX:

- قم بتكوين نسخة من الفئة Diagram.
- قم باستدعاء الأسلوب Save للفئة Diagram لكتابة ملف الرسم Visio إلى VSX.

توضح الصورة أدناه ملف الإخراج VSX. لاحظ أن الإستنسل المستخدم في diagram ، وليس diagram نفسه ، يتم تصديره.

### **تصدير VSD إلى VTX**
TVX هو تمثيل XML لملف قالب ويخزن إعدادات المستند.

لتصدير VSD diagram إلى VTX:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم باستدعاء الأسلوب Save للفئة diagram لكتابة ملف الرسم Visio بتنسيق VTX.

توضح الصورة أدناه ملف الإخراج VTX.

### **التصدير إلى نموذج برمجة XML**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToXML.py" >}}

## **التصدير إلى XPS**
تشرح هذه المقالة كيفية تصدير Microsoft Visio diagram إلى XPS باستخدام Aspose.Diagram لـ Python عبر Java.
استخدم مُنشئ الفئة Diagram لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم.

تأخذ مقتطفات التعليمات البرمجية في هذه المقالة diagram أدناه كمدخل. يمكنك استخدام تنسيقات diagram أخرى (VSS ، VSSX ، VSSM ، VDX ، VST ، VSTX ، VSTM ، VDX ، VTX أو VSX) أيضًا.

لتصدير VSD diagram إلى XPS:

1. قم بتكوين نسخة من الفئة Diagram.
1. اتصل بـ Diagram class "Save method" وقم بتعيين XPS كتنسيق الإخراج.

توضح الصورة أدناه ملف XPS الناتج.

### **التصدير إلى نموذج برمجة XPS**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToXPS.py" >}}

## **تصدير Diagram إلى SVG**
تشرح هذه المقالة كيفية تصدير Microsoft Visio diagram إلى SVG (Scalable Vector Graphics) باستخدام Aspose.Diagram لـ Python عبر Java.

استخدم مُنشئ الفئة Diagram لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم.

لتصدير VSD diagram إلى SVG ، قم بتنفيذ الخطوات التالية:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم باستدعاء طريقة Save للفصل وقم بتعيين SVG كتنسيق تصدير.

### **تصدير Diagram إلى نموذج برمجة SVG**
توضح عينات الكود كيفية تصدير diagram إلى SVG باستخدام Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToSVG.py" >}}

## **تصدير Diagram إلى XAML**
تشرح هذه المقالة كيفية تصدير Microsoft Visio diagram إلى XAML (لغة ترميز التطبيق الموسعة) باستخدام Aspose.Diagram لـ Python عبر Java.

استخدم مُنشئ الفئة Diagram لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم.

لتصدير VSD diagram إلى XAML:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم باستدعاء طريقة Save للفصل وقم بتعيين XAML كتنسيق تصدير.

### **التصدير إلى نموذج برمجة XAML**
يُظهر نموذج التعليمات البرمجية كيفية تصدير diagram إلى XAML باستخدام Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToXAML.py" >}}

## **تحويل Visio الرسم بأشكال انتقائية**
باستخدام Aspose.Diagram API ، يمكن للمطورين تحديد مجموعة من الأشكال لتحويل رسم Visio إلى أي تنسيق مدعوم آخر. تقدم فئة RenderingSaveOptions عضو الأشكال للحفاظ على مجموعة الأشكال. كل فئة خيار حفظ هي الشكل الممتد لفئة RenderingSaveOptions.

لتصدير رسم Visio بأشكال انتقائية:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم بإنشاء مثيل لأي فئة SaveOption لتحديد الإعدادات كما تم سردها
1. استدعاء طريقة حفظ لكائن الفئة Diagram وتمرير كائن فئة خيار الحفظ كمعامل.

### **تحويل Visio الرسم باستخدام عينة برمجة لأشكال انتقائية**
يوضح نموذج التعليمات البرمجية كيفية تصدير رسم بأشكال انتقائية Visio.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ConvertVisioWithSelectiveShapes.py" >}}