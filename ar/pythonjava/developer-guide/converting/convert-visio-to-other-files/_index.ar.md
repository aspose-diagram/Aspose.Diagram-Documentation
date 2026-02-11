---
title:  قم بتحويل Visio إلى تنسيقات أخرى
linktitle:  قم بتحويل Visio إلى تنسيقات أخرى
type: docs
weight: 40
url: /ar/python-java/convert-visio-to-other-files/
description: يوضح لك هذا الموضوع كيفية تحويل تنسيقات Visio إلى SVG،XPS ، XML ، XAML باستخدام Aspose.Diagram لـ Python via Java. ، XAML ببضعة أسطر من الكود.
---
**[للتصدير Microsoft Visio diagram.] (ExportToXML.vsd)**

## **التصدير إلى XML**
تشرح هذه المقالة كيفية تصدير Microsoft Visio diagram إلى XML باستخدام Aspose.Diagram لـ Python via Java.

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

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# 1. Exporting VSDX to VDX
# Call the diagram constructor to load diagram from a VSD file
diagram = Diagram("ExportToXML.vsd")

# Save input VSD as VDX
diagram.save("ExportToXML_Out.vdx", SaveFileFormat.VDX)

# 2. Exporting from VSD to VSX
# Call the diagram constructor to load diagram from a VSD file
        
# Save input VSD as VSX
diagram.save("ExportToXML_Out.vsx", SaveFileFormat.VSX)
        
# 3. Export VSD to VTX
# Save input VSD as VTX
diagram.save("ExportToXML_Out.vtx", SaveFileFormat.VTX)

jpype.shutdownJVM()

{{< /highlight >}}


## **تصدير الى XPS**
توضح هذه المقالة كيفية تصدير Microsoft Visio diagram إلى XPS باستخدام Aspose.Diagram لـ Python via Java.
استخدم مُنشئ الفئة Diagram لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم.

تأخذ مقتطفات التعليمات البرمجية في هذه المقالة diagram أدناه كمدخل. يمكنك استخدام تنسيقات diagram أخرى (VSS ، VSSX ، VSSM ، VDX ، VST ، VSTX ، VSTM ، VDX ، VTX أو VSX) أيضًا.

لتصدير VSD diagram إلى XPS:

1. قم بتكوين نسخة من الفئة Diagram.
1. اتصل بـ Diagram class 'Save method وقم بتعيين XPS كتنسيق الإخراج.

توضح الصورة أدناه ملف الإخراج XPS.

### **التصدير إلى عينة برمجة XPS**

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSD file
diagram = Diagram("ExportToXPS.vsd")

# Save as XPS
diagram.save("ExportToXPS_Out.xps", SaveFileFormat.XPS)

jpype.shutdownJVM()

{{< /highlight >}}


## **تصدير Diagram إلى SVG**
تشرح هذه المقالة كيفية تصدير Microsoft Visio diagram إلى SVG (Scalable Vector Graphics) باستخدام Aspose.Diagram لـ Python via Java.

استخدم مُنشئ الفئة Diagram لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم.

لتصدير VSD diagram إلى SVG ، قم بتنفيذ الخطوات التالية:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم باستدعاء الفئة "Save method" وقم بتعيين SVG كتنسيق التصدير.

### **تصدير عينة برمجية من Diagram إلى SVG**
توضح عينات الكود كيفية تصدير diagram إلى SVG باستخدام Java.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# call the diagram constructor to load diagram from a VSD file
diagram = Diagram("ExportToSVG.vsd")

# Save as SVG
diagram.save("ExportToSVG_Out.svg", SaveFileFormat.SVG)

jpype.shutdownJVM()

{{< /highlight >}}


## **تصدير Diagram إلى XAML**
تشرح هذه المقالة كيفية تصدير Microsoft Visio diagram إلى XAML (لغة ترميز التطبيق الموسعة) باستخدام Aspose.Diagram لـ Python via Java.

استخدم مُنشئ الفئة Diagram لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم.

لتصدير VSD diagram إلى XAML:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم باستدعاء الفئة "Save method" وقم بتعيين XAML كتنسيق التصدير.

### **التصدير إلى عينة برمجة XAML**
يوضح نموذج الكود كيفية تصدير diagram إلى XAML باستخدام Java.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# call the diagram constructor to load diagram from a VSD file
diagram = Diagram("ExportToXAML.vsd")

# save as XAML
diagram.save("ExportToXAML_Out.xaml", SaveFileFormat.XAML)

jpype.shutdownJVM()

{{< /highlight >}}


## **تحويل Visio الرسم بأشكال انتقائية**
باستخدام Aspose.Diagram API ، يمكن للمطورين تحديد مجموعة من الأشكال لتحويل رسم Visio إلى أي تنسيق مدعوم آخر. تقدم فئة RenderingSaveOptions عضو الأشكال للحفاظ على مجموعة الأشكال. كل فئة خيار حفظ هي الشكل الممتد لفئة RenderingSaveOptions.

لتصدير رسم Visio بأشكال انتقائية:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم بإنشاء مثيل لأي فئة SaveOption لتحديد الإعدادات كما تم سردها
1. استدعاء طريقة حفظ لكائن الفئة Diagram وتمرير كائن فئة خيار الحفظ كمعامل.

### **تحويل Visio الرسم باستخدام عينة برمجة لأشكال انتقائية**
يوضح نموذج التعليمات البرمجية كيفية تصدير رسم بأشكال انتقائية Visio.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# call the diagram constructor to load diagram from a VSD file
diagram = Diagram("DrawingSimple.vsdx")

# create an instance SVG save options class
options = SVGSaveOptions()
shapes = options.getShapes()

# get shapes by page index and shape ID, and then add in the shape collection object
shapes.add(diagram.getPages().get(0).getShapes().getShape(1))
shapes.add(diagram.getPages().get(0).getShapes().getShape(2))

# save Visio drawing
diagram.save("SelectiveShapes_out.svg", options)

jpype.shutdownJVM()

{{< /highlight >}}
