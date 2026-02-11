---
title: إنشاء وتخطيط وملاءمة تلقائية الأشكال
type: docs
weight: 10
url: /ar/python-java/create-layout-and-auto-fit-shapes/
---
## **إنشاء Diagram**
 يسمح لك Aspose.Diagram لـ Python via Java بقراءة وإنشاء المخططات Microsoft Visio من داخل التطبيقات الخاصة بك ، بدون أتمتة Microsoft Office. الخطوة الأولى عند تكوين وثائق جديدة هي تكوين diagram. ثم[إضافة الأشكال والموصلات](/diagram/ar/python-java/add-and-connect-visio-shapes/) لبناء diagram. استخدم المُنشئ الافتراضي للفئة Diagram لتكوين diagram جديد.
### **عينة البرمجة**

{{< highlight python >}}
import jpype
import os
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# initialize a new Diagram
diagram = Diagram()
# save in the VSDX format
diagram.save("CreateDiagram_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

## **أشكال التخطيط في نمط المخطط الانسيابي**
 مع أنواع معينة من الرسومات المتصلة ، مثل المخططات الانسيابية والرسومات التخطيطية للشبكة ، يمكنك استخدام ملحق**أشكال التخطيط** ميزة لوضع الأشكال تلقائيًا. يعد تحديد المواقع تلقائيًا أسرع من سحب كل شكل يدويًا إلى موقع جديد.

على سبيل المثال ، إذا كنت تقوم بتحديث مخطط انسيابي كبير لتضمين عملية جديدة ، فيمكنك إضافة الأشكال التي تشكل العملية وتوصيلها ، ثم استخدام ميزة التخطيط لتخطيط الرسم المحدث تلقائيًا.

طريقة Layout ، التي تم الكشف عنها بواسطة تخطيطات فئة Diagram للأشكال و / أو إعادة توجيه الموصلات على جميع صفحات diagram. يقبل هذا الأسلوب كائن LayoutOptions كوسيطة. استخدم الخصائص المختلفة المعروضة بواسطة فئة LayoutOptions لتخطيط الأشكال تلقائيًا.

توضح الصورة أدناه diagram الذي تم تحميله بواسطة مقتطفات التعليمات البرمجية في هذه المقالة ، قبل تطبيق التخطيط التلقائي. توضح مقتطفات التعليمات البرمجية كيفية تطبيق تخطيطات المخطط الانسيابي وتخطيطات الشجرة المضغوطة.

**المصدر diagram.** 

![ما يجب القيام به: image_بديل_نص](create-layout-and-auto-fit-shapes_1.png)

تأخذ مقتطفات التعليمات البرمجية في هذه المقالة المصدر diagram وتطبق عدة أنواع من التخطيط التلقائي عليها ، مع حفظ كل منها في ملف منفصل.

|<p>**تخطيط الأشكال من الأسفل إلى الأعلى** </p><p>![ما يجب القيام به: image_بديل_نص](create-layout-and-auto-fit-shapes_2.png)</p>|<p>**تخطيط الأشكال من أعلى إلى أسفل** </p><p>![ما يجب القيام به: image_بديل_نص](create-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**تخطيط الأشكال من اليسار إلى اليمين** </p><p>![ما يجب القيام به: image_بديل_نص](create-layout-and-auto-fit-shapes_4.png)</p>|<p>**تخطيط الأشكال من اليمين إلى اليسار** </p><p>![ما يجب القيام به: image_بديل_نص](create-layout-and-auto-fit-shapes_5.png)</p>|
لتخطيط الأشكال في نمط المخطط الانسيابي:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم بإنشاء مثيل لفئة LayoutOptions وقم بتعيين الخصائص ذات الصلة بنمط المخطط الانسيابي.
1. قم باستدعاء أسلوب تخطيط الفئة Diagram عن طريق تمرير LayoutOptions.
1. اتصل بـ Diagram class 'طريقة Save لكتابة رسم Visio.
### **عينة برمجة نمط المخطط الانسيابي**

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load an existing Visio diagram
fileName = "LayOutShapesInFlowchartStyle.vdx"
diagram = Diagram(fileName)

# set layout options
flowChartOptions = LayoutOptions()
flowChartOptions.setLayoutStyle(LayoutStyle.FLOW_CHART)
flowChartOptions.setSpaceShapes(1)
flowChartOptions.setEnlargePage(True)

# set layout direction as BottomToTop and then save
flowChartOptions.setDirection(LayoutDirection.BOTTOM_TO_TOP)
diagram.layout(flowChartOptions)
diagram.save("sample_btm_top.vdx", SaveFileFormat.VDX)

# set layout direction as TopToBottom and then save
diagram = Diagram(fileName)
flowChartOptions.setDirection(LayoutDirection.TOP_TO_BOTTOM)
diagram.layout(flowChartOptions)
diagram.save("sample_top_btm.vdx", SaveFileFormat.VDX)

# set layout direction as LeftToRight and then save
diagram = Diagram(fileName)
flowChartOptions.setDirection(LayoutDirection.LEFT_TO_RIGHT)
diagram.layout(flowChartOptions)
diagram.save("sample_left_right.vdx", SaveFileFormat.VDX)

# set layout direction as RightToLeft and then save
diagram = Diagram(fileName)
flowChartOptions.setDirection(LayoutDirection.RIGHT_TO_LEFT)
diagram.layout(flowChartOptions)
diagram.save("sample_right_left.vdx", SaveFileFormat.VDX)

jpype.shutdownJVM()

{{< /highlight >}}

### **تخطيط الأشكال في نمط الشجرة المضغوطة**
يحاول نمط تخطيط الشجرة المضغوط بناء هيكل شجرة. يستخدم نفس ملف الإدخال كما في المثال أعلاه ويحفظ في العديد من أنماط الشجرة المدمجة المختلفة.

|<p>**تخطيط شجرة مضغوط - لأسفل ولليمين** </p><p>![ما يجب القيام به: image_بديل_نص](create-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**تخطيط شجرة مضغوط - لأسفل ولليسار** </p><p>![ما يجب القيام به: image_بديل_نص](create-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**تخطيط شجرة مضغوط - لليمين ولأسفل** </p><p>![ما يجب القيام به: image_بديل_نص](create-layout-and-auto-fit-shapes_8.png)</p>|<p>**تخطيط شجرة مضغوط - لليسار ولأسفل** </p><p>![ما يجب القيام به: image_بديل_نص](create-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
لتخطيط الأشكال في نمط الشجرة المدمجة:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم بإنشاء مثيل لفئة LayoutOptions وقم بتعيين خصائص نمط الشجرة المدمجة.
1. قم باستدعاء أسلوب تخطيط الفئة Diagram عن طريق تمرير LayoutOptions.
1. قم باستدعاء الأسلوب Save للفئة Diagram لكتابة ملف Visio.
#### **عينة برمجة نمط الشجرة المدمجة**

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

        
fileName = "LayOutShapesInCompactTreeStyle.vdx"
# load an existing Visio diagram
diagram = Diagram(fileName)

# set layout options 
compactTreeOptions = LayoutOptions()
compactTreeOptions.setLayoutStyle(LayoutStyle.COMPACT_TREE)
compactTreeOptions.setEnlargePage(True)

# set layout direction as DownThenRight and then save
compactTreeOptions.setDirection(LayoutDirection.DOWN_THEN_RIGHT)
diagram.layout(compactTreeOptions)
diagram.save("sample_down_right.vdx", SaveFileFormat.VDX)

# set layout direction as DownThenLeft and then save
diagram = Diagram(fileName)
compactTreeOptions.setDirection(LayoutDirection.DOWN_THEN_LEFT)
diagram.layout(compactTreeOptions)
diagram.save("sample_down_left.vdx", SaveFileFormat.VDX)

# set layout direction as RightThenDown and then save
diagram = Diagram(fileName)
compactTreeOptions.setDirection(LayoutDirection.RIGHT_THEN_DOWN)
diagram.layout(compactTreeOptions)
diagram.save("sample_right_down.vdx", SaveFileFormat.VDX)

# set layout direction as LeftThenDown and then save
diagram = Diagram(fileName)
compactTreeOptions.setDirection(LayoutDirection.LEFT_THEN_DOWN)
diagram.layout(compactTreeOptions)
diagram.save("sample_left_down.vdx", SaveFileFormat.VDX)

jpype.shutdownJVM()

{{< /highlight >}}

## **احتواء تلقائي Visio Diagram**
Aspose.Diagram API يدعم التركيب التلقائي للرسم Visio. تساعد عملية الميزة هذه على إحضار الأشكال الخارجية داخل حدود الصفحة Visio.

Aspose.Diagram لـ Python via Java API له فئة Diagram التي تمثل رسم Visio. تعرض الفئة DiagramSaveOptions خاصية AutoFitPageToDrawingContent لتلائم رسم Visio تلقائيًا.

هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. قم بإنشاء كائن من فئة DiagramSaveOptions وتمرير تنسيق الملف الناتج.
1. قم بتعيين خاصية AutoFitPageToDrawingContent للكائن DiagramSaveOptions.
1. استدعاء طريقة حفظ لكائن الفئة Diagram وأيضا تمرير مسار الملف الكامل وكائن DiagramSaveOptions.
### **عينة البرمجة الملائمة التلقائية**
يوضح رمز المثال التالي كيفية احتواء الأشكال تلقائيًا في Visio diagram.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load a Visio diagram
diagram = Diagram("BFlowcht.vsdx")

# use saving options
options = DiagramSaveOptions(SaveFileFormat.VSDX)
# set Auto fit page property
options.setAutoFitPageToDrawingContent(True)

# save Visio diagram
diagram.save("AutoFitShapesInVisio_Out.vsdx", options)

jpype.shutdownJVM()

{{< /highlight >}}

## **العمل مع مشروع VBA**
### **تعديل كود وحدة VBA في Visio Diagram**
توضح هذه المقالة كيفية تعديل رمز الوحدة النمطية لـ VBA تلقائيًا باستخدام Aspose.Diagram لـ Python via Java.

لقد أضفنا فئات VbaModule و VbaModuleCollection و VbaProject و VbaProjectReference و VbaProjectReferenceCollection. تساعد هذه الفئات في التحكم في مشروع VBA. يمكن للمطورين استخراج وتعديل رمز الوحدة النمطية لـ VBA.
### **تعديل نموذج برمجة رمز الوحدة النمطية لـ VBA**
الرجاء التحقق من مثال هذا الرمز:


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

diagram = Diagram("Macro.vsdm")
# extract VBA project
v = diagram.getVbaProject()
# Iterate through the modules and modify VBA macro code
for i in range(0, diagram.getVbaProject().getModules().getCount() - 1):
	module = diagram.getVbaProject().getModules().get(i)
	code = module.getCodes()
	if code.contains("This is test message."):
		code = code.replace("This is test message.", "This is Aspose.Diagram message.")
	module.setCodes(code)

# save the Visio diagram
diagram.save("out.vssm", SaveFileFormat.VSSM)

jpype.shutdownJVM()

{{< /highlight >}}

### **قم بإزالة كافة وحدات الماكرو من Visio Diagram**
Aspose.Diagram لـ Python via Java يسمح للمطورين بإزالة كافة وحدات الماكرو من Visio diagram.

تتيح لك خاصية JavaProjectData ، التي تم الكشف عنها بواسطة فئة Diagram ، إزالة كافة وحدات الماكرو من الرسم Visio.
### **قم بإزالة كافة نماذج برمجة وحدات الماكرو**

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load a Visio diagram
diagram = Diagram("Macro.vsdm")

# remove all macros
diagram.setVbProjectData(None)

# Save diagram
diagram.save("RemoveMacrosFromVisio_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

