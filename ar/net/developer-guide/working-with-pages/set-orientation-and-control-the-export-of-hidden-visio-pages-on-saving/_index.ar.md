---
title: قم بتعيين الاتجاه والتحكم في تصدير صفحات Visio المخفية عند الحفظ
type: docs
weight: 20
url: /ar/net/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
description: يوضح هذا القسم كيفية تعيين تخطيط الصفحة باستخدام Aspose.Diagram.
---
## **قم بتغيير نسق الصفحة Visio إلى عمودي أو أفقي**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) يسمح API للمطورين بتعيين اتجاه صفحة الرسم Visio برمجيًا. يشرح موضوع التعليمات هذا كيفية إنجاز هذه المهمة.

 Aspose.Diagram for .NET API لديه[صفحة](http://www.aspose.com/api/net/diagram/aspose.diagram/page) فئة تمثل Visio صفحة رسم. تعرض الخاصية PageSheet بواسطة فئة الصفحة أيضًا خصائص الطباعة. يسمح حقل PrintPageOrientation لخصائص الطباعة بتدوير الصفحة. يوفر ثلاثة خيارات مثل عمودي وأفقي ونفس الشيء كما هو الحال في الطابعة. يمكن تعيين حقل PrintPageOrientation برمجيًا باستخدام Aspose.Diagram API.

هذا المثال يعمل على النحو التالي:

1. قم بتحميل Visio diagram موجود في كائن الفئة Diagram.
1. قم باستخراج صفحة Visio
1. عيّن اتجاهه على أنه عمودي أو أفقي أو نفس الاتجاه على الطابعة.
1. احفظ Visio diagram.
### **تعيين عينة برمجة الاتجاه**
يوضح مثال الكود أدناه كيفية ضبط اتجاه الصفحة Visio.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");
// Page orientation
page.PageSheet.PrintProps.PrintPageOrientation.Value = PrintPageOrientationValue.Landscape;
// Save Visio
diagram.Save(dataDir + "SetPageOrientation_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **التحكم في تصدير الصفحات المخفية Visio عند الحفظ**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API يسمح للمطورين بتضمين أو استبعاد صفحات Visio المخفية عند حفظ ملفات diagram إلى PDF و HTML و Image (PNG و JPEG و GIF) و SVG و XPS. حتى أنها قد تخفي Visio صفحات باستخدام Aspose.Diagram API لأن خيارها متاح بالفعل من خلال الخلية UIVisibility في صفحة ShapeSheet.
### **إخفاء صفحة في Visio Diagram وضبط خيار التصدير**
 Aspose.Diagram for .NET API لديه[صفحة](http://www.aspose.com/api/net/diagram/aspose.diagram/page) فئة تمثل Visio صفحة رسم. تعرض خاصية PageSheet التي تم كشفها بواسطة فئة الصفحة أيضًا خصائص الصفحة. يسمح حقل UIVisibility الخاص بخصائص الصفحة بإخفاء الصفحة. يمكن للمطورين بعد ذلك استخدام خاصية ExportHiddenPage التي تمت إضافتها في فئات SVGSaveOptions و XPSSaveOptions و ImageSaveOptions و HTMLSaveOptions و PdfSaveOptions.
#### **قم بتعيين خيار التصدير لـ PDF**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ تنسيق diagram إلى PDF.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = BOOL.True;

// Initialize PDF save options
PdfSaveOptions options = new PdfSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;

// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToPDF_out.pdf", options);

{{< /highlight >}}
```
#### **قم بتعيين خيار التصدير لـ HTML**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ تنسيق diagram إلى HTML.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = UIVisibilityValue.Visible;

// Initialize PDF save options
HTMLSaveOptions options = new HTMLSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;
// Set export option of comments
options.IsExportComments = false;

// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToHTML_out.html", options);

{{< /highlight >}}
```
#### **اضبط خيار التصدير للصورة**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ diagram إلى تنسيق الصورة.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = UIVisibilityValue.Visible;

// Initialize PDF save options
ImageSaveOptions options = new ImageSaveOptions(SaveFileFormat.JPEG);
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;
// Set export option of comments
options.IsExportComments = false;

// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToImage_out.jpeg", options);

{{< /highlight >}}
```
#### **قم بتعيين خيار التصدير لـ SVG**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ تنسيق diagram إلى SVG.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = UIVisibilityValue.Visible;

// Initialize PDF save options
SVGSaveOptions options = new SVGSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;
// Set export guide shapes 
options.ExportGuideShapes = false;
// Set save format
options.SaveFormat = Aspose.Diagram.SaveFileFormat.SVG;
// Set SVG fit to view port
options.SVGFitToViewPort = true;
// Set export element as Rectangle
options.ExportElementAsRectTag = true;


// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToSVG_out.svg", options);

{{< /highlight >}}
```
#### **قم بتعيين خيار التصدير لـ XPS**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ تنسيق diagram إلى XPS.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = BOOL.True;

// Initialize PDF save options
XPSSaveOptions options = new XPSSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;

// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToXPS_out.xps", options);

{{< /highlight >}}
```
