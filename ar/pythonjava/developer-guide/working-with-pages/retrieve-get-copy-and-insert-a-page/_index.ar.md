---
title: استرداد ، الحصول ، نسخ وإدراج صفحة
type: docs
weight: 10
url: /ar/python-java/retrieve-get-copy-and-insert-a-page/
---
## **استرجاع معلومات الصفحة**
في Microsoft Visio ، تكون الصفحات إما صفحات أمامية أو صفحات خلفية. للحصول على معلومات الصفحة ، على سبيل المثال معرف الصفحة واسم الصفحة ، حدد أولاً ما إذا كانت الصفحة هي خلفية أم صفحة مقدمة.

يمثل العنصر `Page` مساحة الرسم لصفحة أمامية أو صفحة خلفية. تدعم خاصية الصفحات المعروضة بواسطة الفئة `Diagram` مجموعة من كائنات الصفحة. يمكن استخدام هذه الخاصية لاسترداد معلومات الصفحة.

استخدم الخاصية `Page.Background` لتحديد ما إذا كانت الصفحة هي صفحة مقدمة أم خلفية.

### **استرداد نموذج برمجة معلومات الصفحة**
يسترد جزء الكود التالي معلومات الصفحات من diagram.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram
diagram = Diagram("RetrievePageInfo.vdx")

for page in diagram.getPages():
    # Checks if current page is a background page
    if page.getBackground() == BOOL.TRUE:
        # Display information about the background page
        print("Background Page ID : " + str(page.getID()))
        print("Background Page Name : " + str(page.getName()))
    else:
        # Display information about the foreground page
        print("\nPage ID : " + str(page.getID()))
        print("Universal Name : " + str(page.getNameU()))
        print("ID of the Background Page : " + str(page.getBackPage()))

jpype.shutdownJVM()

{{< /highlight >}}


## **احصل على Visio الصفحة من Diagram**
في بعض الأحيان ، يحتاج المطورون إلى الحصول على تفاصيل صفحة رسم Visio. Aspose.Diagram لـ Python via Java له ميزات تساعده على القيام بذلك.

يقدم Aspose.Diagram لـ Python via Java فئة `Diagram` التي تمثل رسم Visio. تدعم خاصية الصفحات المعروضة بواسطة الفئة Diagram مجموعة من `Page` كائنات. تكشف فئة PageCollection عن طريقة `getPage` التي يمكن استدعاؤها للحصول على كائن الصفحة.

### **الحصول على عنصر صفحة Visio بواسطة المعرف**
هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. اتصل على Diagram.Pages class 'getPage method.

يوضح المثال التالي كيفية الحصول على كائن صفحة بواسطة معرف من رسم Visio.

#### **الحصول على كائن الصفحة عن طريق نموذج برمجة المعرف**

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VDX file
diagram = Diagram("DrawingFlowCharts.vsdx")

# Set page id
page_id = 2
# Get page object by id
page2 = diagram.getPages().getPage(page_id)

jpype.shutdownJVM()

{{< /highlight >}}


### **الحصول على Visio صفحة كائن حسب الاسم**
هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. استدعاء Diagram.Pages 'طريقة GetPage.

#### **الحصول على كائن الصفحة حسب نموذج برمجة الاسم**
يوضح المثال التالي كيفية الحصول على كائن صفحة بالاسم من رسم Visio.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSDX file
diagram = Diagram("DrawingFlowCharts.vsdx")

# Set page name
pageName = "Flow 2"
# Get page object by name
page2 = diagram.getPages().getPage(pageName)

jpype.shutdownJVM()

{{< /highlight >}}


## **نسخ صفحة Visio إلى Diagram آخر**
Aspose.Diagram لـ Python via Java API يسمح للمطورين بنسخ وإضافة محتوياته من واحد Visio diagram إلى آخر. يشرح موضوع التعليمات هذا كيفية إنجاز هذه المهمة.

Aspose.Diagram لـ Python via Java API له فئة `Diagram` التي تمثل رسم Visio. تدعم خاصية الصفحات المعروضة بواسطة الفئة Diagram مجموعة من `Page` كائنات. تكشف فئة PageCollection عن طريقة `add` التي يمكن استدعاؤها لإضافة كائن صفحة آخر.

هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر جديد للفئة Diagram.
1. قم بتحميل Visio diagram موجود في كائن الفئة Diagram.
1. أضف كافة الأساتذة من Visio diagram الذي تم تحميله
1. احصل على كائن الصفحة من diagram الذي تم تحميله (والذي يجب نسخه).
1. تعيين اسم كائن الصفحة والمعرف.
1. قم بإزالة الصفحة الفارغة من diagram الجديد (اختياري).
1. طريقة إضافة المكالمة لفئة PageCollection.
1. احفظ diagram الجديد في تخزين الكمبيوتر.

### **نسخ نموذج لبرمجة الصفحة Visio**
يوضح مثال الكود أدناه كيفية نسخ كائن صفحة Visio إلى رسم Visio آخر.


{{< highlight python >}}
import jpype
import asposediagram

jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSD file
originalDiagram = Diagram("Drawing1.vsdx")

# initialize the new visio diagram
newDiagram = Diagram()

# add all masters from the source Visio diagram
originalMasters = originalDiagram.getMasters()
for master in originalMasters:
    newDiagram.addMaster(originalDiagram, master.getName())

# get the page object from the original diagram
SrcPage = originalDiagram.getPages().getPage("Page-1")
# set page name
SrcPage.setName("new page")

# it calculates max page id
max_page_id = 0
if newDiagram.getPages().getCount() != 0:
    max_page_id = newDiagram.getPages().get(0).getID()

for i in range(0, newDiagram.getPages().getCount() - 1):
    if max_page_id < newDiagram.getPages().get(i).getID():
        max_page_id = newDiagram.getPages().get(i).getID()

MaxPageId = max_page_id
# set page id
SrcPage.setID(MaxPageId)
# add reference of the original diagram page
newDiagram.getPages().add(SrcPage)

# remove first empty page
newDiagram.getPages().remove(newDiagram.getPages().get(0))

# save diagram in VDX format
newDiagram.save("CopyVisioPage_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}


## **قم بنسخ Visio صفحة إلى نسخة صفحة أخرى**
تأخذ طريقة `copy` للفئة `Page` نسخة صفحة للنسخ.

``` python
# import diagram

diagram = Diagram(dataDir + "Drawing1.vsdx")

newPage = Page()

# copy page

newPage.copy(diagram.getPages().getPage("Page-1"))

```

## **أدخل صفحة فارغة في رسم Visio**
Aspose.Diagram لـ Python via Java يمكنه إدراج صفحة فارغة جديدة في الرسم Microsoft Office Visio. يصف هذا المثال الموضوع كيفية القيام بذلك.

تسمح طريقة `add` ، المعروضة بواسطة مجموعة الصفحات ، للمطورين بإضافة صفحة فارغة جديدة في Visio diagram. يجب تعيين معرف الصفحة.

### **أدخل نموذج برمجة صفحة فارغة**
يدخل جزء الكود التالي صفحة فارغة في رسم Visio:


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load diagram
diagram = Diagram("Drawing1.vsdx")
        
# it calculates max page id
max_page_id = 0
if diagram.getPages().getCount() != 0:
    max_page_id = diagram.getPages().get(0).getID()

for i in range(0, diagram.getPages().getCount() - 1):
    if max_page_id < diagram.getPages().get(i).getID():
        max_page_id = diagram.getPages().get(i).getID()
        
# Initialize a new page object
newPage = Page()
# Set name
newPage.setName("new page")
# Set page ID
newPage.setID(max_page_id + 1)

# Or try the Page constructor
# Page newPage = Page(MaxPageId + 1)

# Add a new blank page
diagram.getPages().add(newPage)

# Save diagram
diagram.save("InsertBlankPageInVisio_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}


## **انقل موضع الصفحة في الرسم Visio**
Aspose.Diagram لـ Python via Java API يمكنه تحريك موضع الصفحة في الرسم Visio. تساعد طريقة `moveTo` ، التي تم الكشف عنها بواسطة فئة `Page` ، المطورين على تحريك موضع الصفحة.

### **نقل نموذج برمجة موضع الصفحة**
يأخذ عضو MoveTo فهرس الصفحة الهدف كمعامل لتحريك موضع الصفحة في الرسم Visio:

``` python
# import diagram

diagram = Diagram(dataDir + "Drawing1.vsdx")

newPage = Page(1)

# move page in the diagram

newPage.moveTo(2)

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX)
```
