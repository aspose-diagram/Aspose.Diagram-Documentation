---
title: قم بتعيين الاتجاه والتحكم في تصدير صفحات Visio المخفية عند الحفظ
type: docs
weight: 20
url: /ar/python-java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
---
## **قم بتغيير نسق الصفحة Visio إلى عمودي أو أفقي**
Aspose.Diagram لـ Python via Java API يسمح للمطورين بتعيين اتجاه صفحة الرسم Visio برمجيًا. يشرح موضوع التعليمات هذا كيفية إنجاز هذه المهمة.

يحتوي Aspose.Diagram لـ Python via Java API على الفئة `Page` التي تمثل Visio صفحة رسم. تعرض الخاصية PageSheet بواسطة فئة الصفحة أيضًا خصائص الطباعة. يسمح المجال `PrintPageOrientation` لخصائص الطباعة بتدوير الصفحة. يوفر ثلاثة خيارات مثل عمودي وأفقي ونفس الشيء كما هو الحال في الطابعة. يمكن تعيين حقل PrintPageOrientation برمجيًا باستخدام Aspose.Diagram لـ Python via Java API.

هذا المثال يعمل على النحو التالي:

1. قم بتحميل Visio diagram موجود في كائن الفئة Diagram.
1. قم باستخراج صفحة Visio
1. عيّن اتجاهه على أنه عمودي أو أفقي أو نفس الاتجاه على الطابعة.
1. احفظ Visio diagram.

### **تعيين عينة برمجة الاتجاه**
يوضح مثال الكود أدناه كيفية ضبط اتجاه الصفحة Visio.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# initialize the new visio diagram
diagram = Diagram("DrawingFlowCharts.vsdx")

# get Visio page
page = diagram.getPages().getPage("Flow 1")
# page orientation
page.getPageSheet().getPrintProps().getPrintPageOrientation().setValue(PrintPageOrientationValue.LANDSCAPE)
# save Visio
diagram.save("SetPageOrientation_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}


## **التحكم في تصدير الصفحات المخفية Visio عند الحفظ**
Aspose.Diagram لـ Python via Java API يسمح للمطورين بتضمين أو استبعاد الصفحات المخفية Visio عند حفظ diagram إلى PDF ، HTML ، صورة (PNG ، JPEG ، ملفات GIF) ، 0761112481 ، و 0761112481 ، و. حتى أنها قد تخفي Visio صفحات باستخدام Aspose.Diagram لـ Python via Java API لأن خيارها متاح بالفعل من خلال الخلية UIVisibility في صفحة ShapeSheet.

### **إخفاء صفحة في Visio Diagram وضبط خيار التصدير**
يحتوي Aspose.Diagram لـ Python via Java API على الفئة `Page` التي تمثل Visio صفحة رسم. تعرض خاصية PageSheet التي تم كشفها بواسطة فئة الصفحة أيضًا خصائص الصفحة. يسمح المجال `UIVisibility` لخصائص الصفحة بإخفاء الصفحة. يمكن للمطورين بعد ذلك استخدام خاصية `exportHiddenPage` التي تمت إضافتها في فئات `SVGSaveOptions` و `XPSSaveOptions` و `ImageSaveOptions` و `HTMLSaveOptions` و `PdfSaveOptions`.

#### **قم بتعيين خيار التصدير لـ PDF**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ تنسيق diagram إلى PDF.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")
        
# load an existing Visio
diagram = Diagram("DrawingFlowCharts.vsdx")
# get a particular page
page = diagram.getPages().getPage("Flow 2")
# set Visio page visibility
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE)

# initialize PDF save options
options = PdfSaveOptions()
# set export option of hidden Visio pages
options.setExportHiddenPage(False)

# Save the Visio diagram
diagram.save("ExportOfHiddenVisioPagesToPDF_Out.pdf", options)

jpype.shutdownJVM()

{{< /highlight >}}


#### **قم بتعيين خيار التصدير لـ HTML**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ تنسيق diagram إلى HTML.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load an existing Visio
diagram = Diagram("DrawingFlowCharts.vsdx")
# get a particular page
page = diagram.getPages().getPage("Flow 2")
# set Visio page visibility
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE)

# initialize PDF save options
options = HTMLSaveOptions()
# set export option of hidden Visio pages
options.setExportHiddenPage(False)
# set export option of comments
options.setExportComments(False)
# Save the Visio diagram
diagram.save("ExportOfHiddenVisioPagesToHTML_Out.html", options)

jpype.shutdownJVM()

{{< /highlight >}}


#### **اضبط خيار التصدير للصورة**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ diagram إلى تنسيق الصورة.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load an existing Visio
diagram = Diagram("DrawingFlowCharts.vsdx")
# get a particular page
page = diagram.getPages().getPage("Flow 2")
# set Visio page visibility
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE)
# initialize PDF save options
options = ImageSaveOptions(SaveFileFormat.JPEG)
# set export option of hidden Visio pages
options.setExportHiddenPage(False)
# set export option of comments
options.setExportComments(False)

# Save the Visio diagram
diagram.save("ExportOfHiddenVisioPagesToImage_Out.jpeg", options)

jpype.shutdownJVM()

{{< /highlight >}}


#### **قم بتعيين خيار التصدير لـ SVG**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ تنسيق diagram إلى SVG.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load an existing Visio
diagram = Diagram("DrawingFlowCharts.vsdx")
# get a particular page
page = diagram.getPages().getPage("Flow 2")
# set Visio page visibility
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE)

# initialize PDF save options
options = SVGSaveOptions()
# set export option of hidden Visio pages
options.setExportHiddenPage(False)
# Set SVG fit to view port
options.setSVGFitToViewPort(True)
# Set export element as Rectangle
options.setExportElementAsRectTag(True)

# save the Visio diagram
diagram.save("ExportOfHiddenVisioPagesToSVG_Out.svg", options)

jpype.shutdownJVM()

{{< /highlight >}}

