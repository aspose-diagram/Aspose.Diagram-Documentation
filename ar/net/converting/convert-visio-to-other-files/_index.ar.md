---
title:  قم بتحويل Visio إلى تنسيقات أخرى
linktitle:  قم بتحويل Visio إلى تنسيقات أخرى
type: docs
weight: 40
url: /ar/net/convert-visio-to-other-files/
description: يوضح لك هذا الموضوع كيفية السماح Aspose.Diagram بتحويل Visio إلى SVG،XPS ، XML ، XAML تنسيقات. تحويل VSD، VSS، VDW، VST، VSDX، VSSX، VSTX، VSDM، VSTM،VSSM إلى SVG،XPS، XML، XAML مع بضعة أسطر من التعليمات البرمجية.
---
## **تصدير إلى XML**
### **تصدير Microsoft Visio رسم إلى PDF**
توضح عينات الكود كيفية تصدير Microsoft Visio الرسم إلى PDF باستخدام C#.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExportToPDF.vsd");

MemoryStream pdfStream = new MemoryStream();
// Save diagram
diagram.Save(pdfStream, SaveFileFormat.PDF);

// Create a PDF file
FileStream pdfFileStream = new FileStream(dataDir + "ExportToPDF_out.pdf", FileMode.Create, FileAccess.Write);
pdfStream.WriteTo(pdfFileStream);
pdfFileStream.Close();

pdfStream.Close();

// Display Status.
System.Console.WriteLine("Conversion from vsd to pdf performed successfully.");

{{< /highlight >}}


 تشرح هذه المقالة كيفية تصدير Microsoft Visio diagram إلى XML باستخدام[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

- يعرف VDX XML diagram.
- يقوم VTX بتعريف قالب XML.
- يعرف VSX استنسل XML.

 ال[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) قرأ مُنشئو الفئة diagram ويتم استخدام طريقة الحفظ لحفظ أو تصدير diagram بتنسيق ملف مختلف. توضح مقتطفات التعليمات البرمجية في هذه المقالة كيفية استخدام طريقة Save لحفظ ملف Visio في[VDX](https://docs.aspose.com/diagram/net/save-visio-document/), [VTX](https://docs.aspose.com/diagram/net/save-visio-document/) و[VSX](https://docs.aspose.com/diagram/net/save-visio-document/).

توضح الصورة أدناه diagram الذي تم تصديره في قصاصات التعليمات البرمجية أدناه. يظهر الملف الذي تم تصديره قبل كل مقتطف رمز.

|**A Microsoft Visio diagram على وشك التصدير.**|
|:- |
|![ما يجب القيام به: image_بديل_نص](how-to-convert-a-visio-diagram_3.png)|

### **تصدير VSD إلى VDX**
VDX هو تنسيق ملف XML مستند إلى مخطط يسمح لك بحفظ الرسوم التخطيطية بتنسيق يمكن أن تقرأه منتجات بخلاف Microsoft Visio. إنه تنسيق مفيد لنقل المخططات بين تطبيقات البرامج والاحتفاظ بالبيانات القابلة للتحرير.

لتصدير VSD diagram إلى VDX:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم باستدعاء الأسلوب Save للفئة Diagram لكتابة ملف الرسم Visio إلى VDX.

|**الملف VDX الذي تم تصديره.**|
|:- |
|![ما يجب القيام به: image_بديل_نص](how-to-convert-a-visio-diagram_4.png)|

### **تصدير من VSD إلى VSX**
VSX هو نسق XML لتعريف الإستنسل ، الكائنات الأساسية التي تم بناء diagram منها. عند تحويل ملف Visio إلى VSX ، يتم تصدير قوالب الإستنسل فقط.

لتصدير VSD diagram إلى VSX:

- قم بتكوين نسخة من الفئة Diagram.
- قم باستدعاء الأسلوب Save للفئة Diagram لكتابة ملف الرسم Visio إلى VSX.
### **تصدير VSD إلى VTX**
TVX هو تمثيل XML لملف قالب ويخزن إعدادات المستند.

لتصدير VSD diagram إلى VTX:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم باستدعاء الأسلوب Save للفئة diagram لكتابة ملف الرسم Visio بتنسيق VTX.
### **تصدير Microsoft Visio الرسم إلى XML**
توضح نماذج التعليمات البرمجية كيفية تصدير Microsoft Visio الرسم إلى XML باستخدام C#.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
            
/* 1. Exporting VSDX to VDX */
// Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToXML.vsd");

// Save input VSD as VDX
diagram.Save(dataDir + "ExportToXML_out.vdx", SaveFileFormat.VDX);

/* 2. Exporting from VSD to VSX */
// Call the diagram constructor to load diagram from a VSD file
            
// Save input VSD as VSX
diagram.Save(dataDir + "ExportToXML_out.vsx", SaveFileFormat.VSX);
            
/* 3. Export VSD to VTX */
// Save input VSD as VTX
diagram.Save(dataDir + "ExportToXML_out.vtx", SaveFileFormat.VTX);

{{< /highlight >}}


## **تصدير إلى XPS**
 يشرح هذا المقال كيفية تصدير Microsoft Visio diagram إلى XPS باستخدام[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.
 استخدم ال[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) مُنشئ class لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم.

تأخذ مقتطفات التعليمات البرمجية في هذه المقالة diagram أدناه كمدخل. يمكنك استخدام تنسيقات diagram أخرى (VSS ، VSSX ، VSSM ، VDX ، VST ، VSTX ، VDX ، VTX أو VSX) أيضًا.

|**وثيقة المصدر.**|
|:- |
|![ما يجب القيام به: image_بديل_نص](how-to-convert-a-visio-diagram_5.png)|


لتصدير VSD diagram إلى XPS:

1. قم بتكوين نسخة من الفئة Diagram.
1. اتصل بـ Diagram class 'Save method وقم بتعيين XPS كتنسيق الإخراج.
### **تصدير Microsoft Visio رسم إلى XPS**
توضح عينات الكود كيفية تصدير Microsoft Visio الرسم إلى XPS باستخدام C#.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Open a VSD file
Diagram diagram = new Diagram(dataDir + "LayOutShapesInCompactTreeStyle.vdx");

// Save diagram to an XPS format
diagram.Save(dataDir + "ExportToXPS_out.xps", SaveFileFormat.XPS);

{{< /highlight >}}


## **قم بتصدير Diagram إلى SVG**
 تشرح هذه المقالة كيفية تصدير Microsoft Visio diagram إلى SVG (Scalable Vector Graphics) باستخدام[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

 استخدم ال[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) مُنشئ class لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم.

لتصدير VSD diagram إلى SVG ، قم بتنفيذ الخطوات التالية:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم باستدعاء الفئة "Save method" وقم بتعيين SVG كتنسيق التصدير.
### **تصدير Microsoft Visio رسم إلى SVG**
توضح عينات الكود كيفية تصدير diagram إلى SVG باستخدام C#.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExportToSVG.vsd");

// Save SVG Output file
diagram.Save(dataDir + "Output.svg", SaveFileFormat.SVG);

{{< /highlight >}}

## **تصدير إلى SWF**
 يشرح هذا المقال كيفية تصدير Microsoft Visio diagram إلى SWF باستخدام[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

 استخدم ال[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)class 'builders' لقراءة ملفات diagram ثم طريقة Save للفئة Diagram لتصدير تنسيق diagram إلى SWF. تُظهر الصورة أدناه ملف الإدخال VSD الذي يعرضه الكود إلى SWF. يمكنك استخدام تنسيقات diagram أخرى (VSS ، VSSX ، VSSM ، VDW ، VDX ، VST ، VSTX ، VSTM ، VDX ، VSX أو VSX أو VTX)

|**المدخلات diagram.**|
|:- |
|![ما يجب القيام به: image_بديل_نص](how-to-convert-a-visio-diagram_7.png)|

بعد الكود ، هناك صورة للمخرج.

لتصدير VSD diagram إلى SWF:

- قم بتكوين نسخة من الفئة Diagram.
- اتصل بـ Diagram class 'Save method وقم بتوفير تنسيق SWF لتصدير diagram إلى SWF.
### **نموذج برمجة العارض المضمن**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();
// Load diagram
Diagram diagram = new Diagram(dataDir + "ActvDir.vsd");
// Save diagram
diagram.Save(dataDir + "Output_out.swf", SaveFileFormat.SWF);

{{< /highlight >}}

### **بدون نموذج برمجة العارض**
يتضمن الملف SWF الذي تم إنشاؤه بواسطة قصاصات التعليمات البرمجية هذه عارض SWF. استبعاد عارض SWF من الملف باستخدام التعليمات البرمجية التالية.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Instantiate Diagram Object and open VSD file
Diagram diagram = new Diagram(dataDir + "ExportToSWFWithoutViewer.vsd");

// Instantiate the Save Options
SWFSaveOptions options = new SWFSaveOptions();

// Set Save format as SWF
options.SaveFormat = SaveFileFormat.SWF;

// Exclude the embedded viewer
options.ViewerIncluded = false;

// Save the resultant SWF file
diagram.Save(dataDir + "ExportToSWFWithoutViewer_out.swf", SaveFileFormat.SWF);

{{< /highlight >}}

## **قم بتصدير Diagram إلى XAML**
تشرح هذه المقالة كيفية تصدير Microsoft Visio diagram إلى XAML (لغة ترميز التطبيق الموسعة) باستخدام[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

 استخدم ال[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) مُنشئ class لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم.

لتصدير VSD diagram إلى XAML:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم باستدعاء الفئة "Save method" وقم بتعيين XAML كتنسيق التصدير.
### **تصدير Microsoft Visio رسم إلى XAML**
يوضح نموذج الكود كيفية تصدير diagram إلى XAML باستخدام C#.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
// Load diagram
Diagram diagram = new Diagram(dataDir + "ExportToXAML.vsd");
// Save diagram
diagram.Save(dataDir + "ExportToXAML_out.xaml", SaveFileFormat.XAML);

{{< /highlight >}}

## **تحويل Visio الرسم بأشكال انتقائية**
باستخدام Aspose.Diagram API ، يمكن للمطورين تحديد مجموعة من الأشكال لتحويل رسم Visio إلى أي تنسيق مدعوم آخر. تقدم فئة RenderingSaveOptions عضو الأشكال للحفاظ على مجموعة الأشكال. كل فئة خيار حفظ هي الشكل الممتد لفئة RenderingSaveOptions.

لتصدير رسم Visio بأشكال انتقائية:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم بإنشاء مثيل لأي فئة SaveOption لتحديد الإعدادات كما تم سردها هنا:[حدد Visio خيارات الحفظ](https://docs.aspose.com/diagram/net/save-visio-document/#specifying-visio-save-options)
1. طريقة Call Save لعنصر فئة Diagram وتمرير كائن فئة خيار الحفظ كمعامل.
### **تحويل Visio الرسم باستخدام عينة برمجة لأشكال انتقائية**
يوضح نموذج التعليمات البرمجية كيفية تصدير رسم بأشكال انتقائية Visio.


{{< highlight csharp >}}
// the path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance SVG save options class
SVGSaveOptions options = new SVGSaveOptions();
ShapeCollection shapes = options.Shapes;

// get shapes by page index and shape ID, and then add in the shape collection object
shapes.Add(diagram.Pages[0].Shapes.GetShape(1));
shapes.Add(diagram.Pages[0].Shapes.GetShape(2));

// save Visio drawing
diagram.Save(dataDir + "SelectiveShapes_out.svg", options);
{{< /highlight >}}
