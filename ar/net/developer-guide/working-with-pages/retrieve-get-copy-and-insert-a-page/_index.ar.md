---
title: استرداد ، الحصول ، نسخ وإدراج صفحة
type: docs
weight: 10
url: /ar/net/retrieve-get-copy-and-insert-a-page/
description: يشرح هذا القسم كيفية إدراج صفحة أو نسخها أو الحصول على معلومات الصفحة باستخدام Aspose.Diagram.
---
## **استرجاع معلومات الصفحة**
في Microsoft Visio ، تكون الصفحات إما صفحات أمامية أو صفحات خلفية. للحصول على معلومات الصفحة ، على سبيل المثال معرف الصفحة واسم الصفحة ، حدد أولاً ما إذا كانت الصفحة هي خلفية أم صفحة مقدمة.

 ال[صفحة](http://www.aspose.com/api/net/diagram/aspose.diagram/page)يمثل الكائن منطقة الرسم لصفحة أمامية أو صفحة خلفية. خاصية الصفحات التي يعرضها ملف[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) فئة تدعم مجموعة من Aspose.Diagram.Page كائنات. يمكن استخدام هذه الخاصية لاسترداد معلومات الصفحة.

استخدم خاصية Page.Background لتحديد ما إذا كانت الصفحة مقدمة أم صفحة خلفية.
### **استرداد نموذج برمجة معلومات الصفحة**
يسترد جزء الكود التالي معلومات الصفحات من diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Call the diagram constructor to load diagram from a VDX file
Diagram vdxDiagram = new Diagram(dataDir + "RetrievePageInfo.vdx");

foreach (Aspose.Diagram.Page page in vdxDiagram.Pages)
{
    // Checks if current page is a background page
    if (page.Background == Aspose.Diagram.BOOL.True)
    {
        // Display information about the background page
        Console.WriteLine("Background Page ID : " + page.ID);
        Console.WriteLine("Background Page Name : " + page.Name);
    }
    else
    {
        // Display information about the foreground page
        Console.WriteLine("\nPage ID : " + page.ID);
        Console.WriteLine("Universal Name : " + page.NameU);
        Console.WriteLine("ID of the Background Page : " + page.BackPage);
    }
}

{{< /highlight >}}
```
## **احصل على Visio الصفحة من Diagram**
في بعض الأحيان ، يحتاج المطورون إلى الحصول على تفاصيل صفحة رسم Visio. Aspose.Diagram له ميزات تساعدهم على القيام بذلك.

 يقدم Aspose.Diagram for .NET[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) فئة تمثل رسم Visio. تدعم خاصية الصفحات المعروضة بواسطة فئة Diagram مجموعة من كائنات Aspose.Diagram.Page. تكشف فئة PageCollection عن أسلوب GetPage الذي يمكن استدعاؤه للحصول على كائن الصفحة.
### **الحصول على عنصر صفحة Visio بواسطة المعرف**
هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. استدعاء Diagram.Pages 'طريقة GetPage.

يوضح المثال التالي كيفية الحصول على كائن صفحة بواسطة معرف من رسم Visio.
#### **الحصول على كائن الصفحة عن طريق نموذج برمجة المعرف**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page id
int pageid = 2;
// Get page object by id
Page page2 = diagram.Pages.GetPage(pageid);

{{< /highlight >}}
```
### **الحصول على Visio صفحة كائن حسب الاسم**
هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. استدعاء Diagram.Pages 'طريقة GetPage.
#### **الحصول على كائن الصفحة حسب نموذج برمجة الاسم**
يوضح المثال التالي كيفية الحصول على كائن صفحة بالاسم من رسم Visio.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page name
string pageName = "Flow 2";
// Get page object by name
Page page2 = diagram.Pages.GetPage(pageName);

{{< /highlight >}}
```
## **نسخ صفحة Visio إلى Diagram آخر**
Aspose.Diagram for .NET API يسمح للمطورين بنسخ وإضافة محتوياته من Visio diagram إلى آخر. يشرح موضوع التعليمات هذا كيفية إنجاز هذه المهمة.

 Aspose.Diagram for .NET API لديه[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) فئة تمثل رسم Visio. تدعم خاصية الصفحات المعروضة بواسطة فئة Diagram مجموعة من كائنات Aspose.Diagram.Page. تكشف فئة PageCollection عن طريقة Add التي يمكن استدعاؤها لإضافة كائن صفحة آخر.

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

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram NewDigram = new Diagram();

// Load source diagram
Diagram dgm = new Diagram(dataDir + "Drawing1.vsdx");
// Add all masters from the source Visio diagram
foreach (Master master in dgm.Masters)
    NewDigram.Masters.Add(master);

// Get page object
Aspose.Diagram.Page SrcPage = dgm.Pages.GetPage("Page-1");
// Set name
SrcPage.Name = "new page";

// It calculates max page id
int max = 0;
if (NewDigram.Pages.Count != 0)
    max = NewDigram.Pages[0].ID;

for (int i = 1; i < NewDigram.Pages.Count; i++)
{
    if (max < NewDigram.Pages[i].ID)
        max = NewDigram.Pages[i].ID;
}
            
// Set max page ID 
int MaxPageId = max;
// Set page ID
SrcPage.ID = MaxPageId + 1;

// Add page from the source diagram
NewDigram.Pages.Add(SrcPage);
// Remove first empty page
NewDigram.Pages.Remove(NewDigram.Pages[0]);
// Save diagram
NewDigram.Save(dataDir + "CopyVisioPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **قم بنسخ Visio صفحة إلى نسخة صفحة أخرى**
تأخذ طريقة النسخ الخاصة بفئة الصفحة نسخة صفحة ليتم نسخها.

**C#**

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page();

// copy page

newPage.Copy(diagram.Pages.GetPage("Page-1"));

{{< /highlight >}}
## **أدخل صفحة فارغة في رسم Visio**
[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) يمكن إدراج صفحة فارغة جديدة في الرسم Microsoft Office Visio. يصف هذا المثال الموضوع كيفية القيام بذلك.

يسمح أسلوب Add ، الذي تم عرضه بواسطة مجموعة Pages ، للمطورين بإضافة صفحة فارغة جديدة في diagram Visio. يجب تعيين معرف الصفحة.
### **أدخل نموذج برمجة صفحة فارغة**
يدخل جزء الكود التالي صفحة فارغة في رسم Visio:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// It calculates max page id
int max = 0;
if (diagram.Pages.Count != 0)
    max = diagram.Pages[0].ID;

for (int i = 1; i < diagram.Pages.Count; i++)
{
    if (max < diagram.Pages[i].ID)
        max = diagram.Pages[i].ID;
}

// Set max page ID
int MaxPageId = max;

// Initialize a new page object
Page newPage = new Page();
// Set name
newPage.Name = "new page";
// Set page ID
newPage.ID = MaxPageId + 1;

// Or try the Page constructor
// Page newPage = new Page(MaxPageId + 1);

// Add a new blank page
diagram.Pages.Add(newPage);

// Save diagram
diagram.Save(dataDir + "InsertBlankPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **انقل موضع الصفحة في الرسم Visio**
Aspose.Diagram for .NET API يمكنه تحريك موضع الصفحة في الرسم Visio. تساعد طريقة MoveTo ، التي تعرضها فئة الصفحة ، المطورين على تحريك موضع الصفحة.
### **نقل نموذج برمجة موضع الصفحة**
يأخذ عضو MoveTo فهرس الصفحة الهدف كمعامل لتحريك موضع الصفحة في الرسم Visio:

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.MoveTo(2);

diagram.Save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
