---
title: استرداد ، الحصول ، نسخ وإدراج صفحة
type: docs
weight: 10
url: /ar/java/retrieve-get-copy-and-insert-a-page/
---
## **استرجاع معلومات الصفحة**
في Microsoft Visio ، تكون الصفحات إما صفحات أمامية أو صفحات خلفية. للحصول على معلومات الصفحة ، على سبيل المثال معرف الصفحة واسم الصفحة ، حدد أولاً ما إذا كانت الصفحة هي خلفية أم صفحة مقدمة.

 ال[صفحة](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page)يمثل الكائن منطقة الرسم لصفحة أمامية أو صفحة خلفية. خاصية الصفحات التي يعرضها ملف[Diagram](https://reference.aspose.com/diagram/java) فئة تدعم مجموعة من Aspose.Diagram.Page كائنات. يمكن استخدام هذه الخاصية لاسترداد معلومات الصفحة.

استخدم خاصية Page.Background لتحديد ما إذا كانت الصفحة مقدمة أم صفحة خلفية.

توضح الصورة أدناه الإخراج من مقتطفات التعليمات البرمجية في هذه المقالة.

**وحدة تحكم تظهر الإخراج.** 

![ما يجب القيام به: image_بديل_نص](retrieve-get-copy-and-insert-a-page_1.png)
### **استرداد نموذج برمجة معلومات الصفحة**
يسترد جزء الكود التالي معلومات الصفحات من diagram.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrievePageInfo.class);

//Call the diagram constructor to load diagram
Diagram diagram = new Diagram(dataDir+ "RetrievePageInfo.vdx");

for (Page page : (Iterable<Page>) diagram.getPages())
{
    //Checks if current page is a background page
    if (page.getBackground() == com.aspose.diagram.BOOL.TRUE)
    {
        //Display information about the background page
        System.out.println("Background Page ID : " + page.getID());
        System.out.println("Background Page Name : " + page.getName());
    }
    else
    {
        //Display information about the foreground page
        System.out.println("\nPage ID : " + page.getID());
        System.out.println("Universal Name : " + page.getNameU());
        System.out.println("ID of the Background Page : " + page.getBackPage());
    }
}

{{< /highlight >}}

## **احصل على Visio الصفحة من Diagram**
في بعض الأحيان ، يحتاج المطورون إلى الحصول على تفاصيل صفحة رسم Visio. Aspose.Diagram له ميزات تساعدهم على القيام بذلك.

 يقدم Aspose.Diagram for Java[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) فئة تمثل رسم Visio. تدعم خاصية الصفحات المعروضة بواسطة فئة Diagram مجموعة من كائنات Aspose.Diagram.Page. تكشف فئة PageCollection عن أسلوب GetPage الذي يمكن استدعاؤه للحصول على كائن الصفحة.
### **الحصول على عنصر صفحة Visio بواسطة المعرف**
هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. استدعاء Diagram.Pages 'طريقة GetPage.

يوضح المثال التالي كيفية الحصول على كائن صفحة بواسطة معرف من رسم Visio.
#### **الحصول على كائن الصفحة عن طريق نموذج برمجة المعرف**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetVisioPagebyID.class); 
// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page id
int pageid = 2;
// Get page object by id
Page page2 = diagram.getPages().getPage(pageid);

{{< /highlight >}}

### **الحصول على Visio صفحة كائن حسب الاسم**
هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. استدعاء Diagram.Pages 'طريقة GetPage.
#### **الحصول على كائن الصفحة حسب نموذج برمجة الاسم**
يوضح المثال التالي كيفية الحصول على كائن صفحة بالاسم من رسم Visio.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetVisioPagebyName.class);     
// Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page name
String pageName = "Flow 2";
// Get page object by name
Page page2 = diagram.getPages().getPage(pageName);

{{< /highlight >}}

## **نسخ صفحة Visio إلى Diagram آخر**
Aspose.Diagram for Java API يسمح للمطورين بنسخ وإضافة محتوياته من Visio diagram إلى آخر. يشرح موضوع التعليمات هذا كيفية إنجاز هذه المهمة.

 Aspose.Diagram for Java API لديه[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) فئة تمثل رسم Visio. تدعم خاصية الصفحات المعروضة بواسطة فئة Diagram مجموعة من كائنات Aspose.Diagram.Page. تكشف فئة PageCollection عن طريقة Add التي يمكن استدعاؤها لإضافة كائن صفحة آخر.

هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر جديد للفئة Diagram.
1. قم بتحميل Visio diagram موجود في كائن الفئة Diagram.
1. أضف كافة الأساتذة من Visio diagram الذي تم تحميله
1. احصل على كائن الصفحة من diagram الذي تم تحميله (والذي يجب نسخه).
1. تعيين اسم كائن الصفحة والمعرف.
1. قم بإزالة الصفحة الفارغة من diagram الجديد (اختياري).
1. طريقة Call Add من فئة PageCollection.
1. احفظ diagram الجديد في تخزين الكمبيوتر.
### **نسخ نموذج لبرمجة الصفحة Visio**
يوضح مثال الكود أدناه كيفية نسخ كائن صفحة Visio إلى رسم Visio آخر.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CopyVisioPage.class);
        
// Call the diagram constructor to load diagram from a VSD file
Diagram originalDiagram = new Diagram(dataDir + "Drawing1.vsd");

// initialize the new visio diagram
Diagram newDiagram = new Diagram();

// add all masters from the source Visio diagram
MasterCollection originalMasters = originalDiagram.getMasters();
for (Master master : (Iterable<Master>) originalMasters) {
   newDiagram.addMaster(originalDiagram, master.getName());
}

// get the page object from the original diagram
Page SrcPage = originalDiagram.getPages().getPage("Page-1");
// set page name
SrcPage.setName("new page");
        
// it calculates max page id
int max = 0;
if (newDiagram.getPages().getCount() != 0)
    max = newDiagram.getPages().get(0).getID();

for (int i = 1; i < newDiagram.getPages().getCount(); i++)
{
    if (max < newDiagram.getPages().get(i).getID())
        max = newDiagram.getPages().get(i).getID();
}
       
int MaxPageId = max;
// set page id
SrcPage.setID(MaxPageId);
// add reference of the original diagram page
newDiagram.getPages().add(SrcPage);

// remove first empty page
newDiagram.getPages().remove(newDiagram.getPages().get(0));

// save diagram in VDX format
newDiagram.save(dataDir + "CopyVisioPage_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **قم بنسخ Visio صفحة إلى نسخة صفحة أخرى**
تأخذ طريقة النسخ الخاصة بفئة الصفحة نسخة صفحة ليتم نسخها.

**Java**

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page();

// copy page

newPage.copy(diagram.getPages().getPage("Page-1"));

{{< /highlight >}}
## **أدخل صفحة فارغة في رسم Visio**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) يمكن إدراج صفحة فارغة جديدة في الرسم Microsoft Office Visio. يصف هذا المثال الموضوع كيفية القيام بذلك.

يسمح أسلوب Add ، الذي تم عرضه بواسطة مجموعة Pages ، للمطورين بإضافة صفحة فارغة جديدة في diagram Visio. يجب تعيين معرف الصفحة.
### **أدخل نموذج برمجة صفحة فارغة**
يدخل جزء الكود التالي صفحة فارغة في رسم Visio:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(InsertBlankPageInVisio.class);   
// load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
        
// it calculates max page id
int max = 0;
if (diagram.getPages().getCount() != 0)
    max = diagram.getPages().get(0).getID();

for (int i = 1; i < diagram.getPages().getCount(); i++)
{
    if (max < diagram.getPages().get(i).getID())
        max = diagram.getPages().get(i).getID();
}
        
// Initialize a new page object
Page newPage = new Page();
// Set name
newPage.setName("new page");
// Set page ID
newPage.setID(max + 1);

// Or try the Page constructor
// Page newPage = new Page(MaxPageId + 1);

// Add a new blank page
diagram.getPages().add(newPage);

// Save diagram
diagram.save(dataDir + "InsertBlankPageInVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **انقل موضع الصفحة في الرسم Visio**
Aspose.Diagram for Java API يمكنه تحريك موضع الصفحة في الرسم Visio. تساعد طريقة moveTo ، التي تعرضها فئة الصفحة ، المطورين على تحريك موضع الصفحة.
### **نقل نموذج برمجة موضع الصفحة**
يأخذ عضو MoveTo فهرس الصفحة الهدف كمعامل لتحريك موضع الصفحة في الرسم Visio:

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.moveTo(2);

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
