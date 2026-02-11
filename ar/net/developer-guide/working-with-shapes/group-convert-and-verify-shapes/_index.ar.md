---
title: تجميع وتحويل والتحقق من الأشكال
type: docs
weight: 80
url: /ar/net/group-convert-and-verify-shapes/
description: يشرح هذا القسم كيفية تجميع الأشكال باستخدام Aspose.Diagram.
---
## **قم بتجميع الأشكال المتعددة معًا في رسم Visio**
Aspose.Diagram API يسمح للمطورين بتجميع الأشكال معًا لنقلها جميعًا مرة واحدة. يحتفظ كل شكل في المجموعة بهوية فريدة وله مجموعة خصائصه الخاصة. عندما نغير تنسيق مجموعة من الأشكال ، فإنه يعين الخاصية الجديدة لكل شكل.
### **كيفية تجميع الأشكال**
 طريقة المجموعة المعروضة من قبل[ShapeCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) يمكن استخدام فئة لتجميع الأشكال معًا.

يوضح الكود أدناه كيفية:

1. تحميل عينة diagram.
1. تهيئة مجموعة من الأشكال
1. الحصول على شكل معين بواسطة معرف.
1. الحصول على شكل معين آخر بواسطة معرف.
1. تعيين الأشكال للمصفوفة.
1. تجميع الأشكال عن طريق استدعاء طريقة المجموعة.
1. احفظ diagram
#### **عينة برمجة الأشكال الجماعية**
استخدم الكود التالي في تطبيق .NET لتجميع الأشكال معًا باستخدام Aspose.Diagram for .NET API.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

// Initialize an array of shapes
Aspose.Diagram.Shape[] ss = new Aspose.Diagram.Shape[3];

// Extract and assign shapes to the array
ss[0] = page.Shapes.GetShape(15);
ss[1] = page.Shapes.GetShape(16);
ss[2] = page.Shapes.GetShape(17);

// Mark array shapes as group
page.Shapes.Group(ss);

// Save visio diagram
diagram.Save(dataDir + "GroupShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **تحويل شكل Visio إلى تنسيقات ملفات أخرى**
Aspose.Diagram for .NET API يسمح للمطورين بتحويل شكل Visio واحد إلى أي تنسيق ملف آخر مدعوم. في هذه المقالة ، نقوم بإزالة جميع أشكال Visio الأخرى من الصفحة وتخصيص إعداد الصفحة وفقًا لحجم الشكل المصدر.
### **تحويل شكل Visio معين**
 يمكن للمطورين تحويل شكل Visio إلى PDF و HTML و Image و SVG و SWF بواسطة**تحديد خيارات الحفظ Visio**.
يعمل رمز المثال هذا على النحو التالي:

1. قم بتحميل المصدر Visio.
1. احصل على صفحة معينة.
1. قم بإزالة صفحة الخلفية.
1. قم بإنشاء جدول تجزئة لجميع الأشكال التي تحتوي على المعرفات والأسماء.
1. كرر من خلال جدول التجزئة
1. قم بإزالة كافة الأشكال من صفحة Visio ، باستثناء الشكل المعين.
1. اضبط حجم الصفحة.
1. احفظ الصفحة Visio بأي تنسيق ملف مدعوم.
#### **تحويل نموذج برمجة الشكل**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");

double shapeWidth = 0;
double shapeHeight = 0;

// Get Visio page
Aspose.Diagram.Page srcPage = srcVisio.Pages.GetPage("Page-3");
// Remove background page
srcPage.BackPage = null;

// Get hash table of shapes, it holds id and name
Hashtable remShapes = new Hashtable();
// Hashtable<Long, String> remShapes = new Hashtable<Long, String>();
foreach (Aspose.Diagram.Shape shape in srcPage.Shapes)
    // For the normal shape
    remShapes.Add(shape.ID, shape.Name);

// Iterate through the hash table
foreach (DictionaryEntry shapeEntry in remShapes)
{
    long key = (long)shapeEntry.Key;
    string val = (string)shapeEntry.Value;
    Aspose.Diagram.Shape shape = srcPage.Shapes.GetShape(key);
    // Check of the shape name
    if (val.Equals("GroupShape1"))
    {
        // Move shape to the origin corner
        shapeWidth = shape.XForm.Width.Value;
        shapeHeight = shape.XForm.Height.Value;
        shape.MoveTo(shapeWidth * 0.5, shapeHeight * 0.5);
        // Trim page size
        srcPage.PageSheet.PageProps.PageWidth.Value = shapeWidth;
        srcPage.PageSheet.PageProps.PageHeight.Value = shapeHeight;
    }
    else
    {
        // Remove shape from the Visio page and hash table
        srcPage.Shapes.Remove(shape);
    }
}
remShapes.Clear();

// Specify saving options
Aspose.Diagram.Saving.PdfSaveOptions opts = new Aspose.Diagram.Saving.PdfSaveOptions();
// Set page count to save
opts.PageCount = 1;
// Set starting index of the page
opts.PageIndex = 1;
// Save it
srcVisio.Save(dataDir + "SaveVisioShapeInOtherFormats_out.pdf", opts);

{{< /highlight >}}
```
### **حوّل Visio إلى PDF**
تسمح طريقة ToPdf لفئة الشكل بتحويل شكل إلى تنسيق PDF.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **حوّل Visio إلى HTML**
تسمح طريقة ToHTML لفئة الشكل بتحويل شكل إلى تنسيق HTML.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}
## **تحقق مما إذا كان شكلا Visio متصل أو ملتصق**
 Aspose.Diagram for .NET API يسمح للمطورين بالتحقق من أن الشكلين Visio ملتصقان أو متصلان. في السابق ، رأينا كيف يمكننا توصيل شكلين أو لصقهما في موضوعات المساعدة هذه:[إضافة وتوصيل Visio الأشكال](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) و[أشكال الغراء داخل الحاوية](/diagram/ar/net/working-with-shapes-gluing/).
### **التحقق من الأشكال المتصلة أو الملصقة**
 ال[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) تقدم الفئة خصائص IsGlued و IsConnected لتحديد ما إذا كان الشكلين ملتصقين أم متصلين.
#### **التحقق من نموذج برمجة الأشكال المتصلة أو الملصقة**
يتحقق الجزء التالي من الكود مما إذا كان الشكلين متصلين أم تم لصقهما.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Set two shape ids
long ShapeIdOne = 15;
long ShapeIdTwo = 16;

// Get Visio page by name
Page page = diagram.Pages.GetPage("Page-3");

// Get Visio shapes by ids
Shape ShapedOne = page.Shapes.GetShape(ShapeIdOne);
Shape ShapedTwo = page.Shapes.GetShape(ShapeIdTwo);

// Determine whether shapes are connected
bool connected = ShapedOne.IsConnected(ShapedTwo);
Console.WriteLine("Shapes are connected: " + connected);

// Determine whether shapes are glued
bool glued = ShapedOne.IsGlued(ShapedTwo);
Console.WriteLine("Shapes are Glued: " + glued);

{{< /highlight >}}
```
## **تحقق مما إذا كان الشكل Visio في مجموعة من الأشكال**
Aspose.Diagram for .NET API يسمح للمطورين بالتحقق من أن الشكل Visio موجود في مجموعة من الأشكال أم لا.
### **التحقق من الشكل في مجموعة الأشكال**
ال[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)تقدم الفئة خصائص IsInGroup لتحديد ما إذا كان الشكل Visio في شكل مجموعة.
#### **التحقق من الشكل في عينة برمجة مجموعة الأشكال**
يتحقق جزء التعليمات البرمجية التالي مما إذا كان الشكل في شكل مجموعة.

```
{{< highlight "csharp" >}}
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(13).Shapes.GetShape(2);
Console.WriteLine("Is it in a Group: " + shape.IsInGroup());
{{< /highlight >}}
```
