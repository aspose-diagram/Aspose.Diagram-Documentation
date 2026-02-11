---
title: إنشاء وتحديث وتخطيط وملاءمة تلقائية الأشكال
type: docs
weight: 10
url: /ar/net/create-update-layout-and-auto-fit-shapes/
description: استخدم C# Diagram API لإنشاء أشكال التخطيط التلقائي وتحديثها في ملفات Visio باستخدام C# داخل تطبيقاتك. دليل كامل مع C# عينات كود.
---
## **إنشاء Diagram**
 يتيح لك Aspose.Diagram for .NET قراءة وإنشاء Microsoft Visio الرسوم التخطيطية من داخل التطبيقات الخاصة بك ، بدون أتمتة Microsoft Office. الخطوة الأولى عند تكوين وثائق جديدة هي تكوين diagram. ثم[إضافة الأشكال والموصلات](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/)لإنشاء diagram. استخدم المُنشئ الافتراضي لـ[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) فئة لإنشاء diagram جديد.
### **عينة البرمجة**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Create directory if it is not already present.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Initialize a new Visio
Diagram diagram = new Diagram();
dataDir = dataDir + "CreateDiagram_out.vsdx";
// Save in the VSDX format
diagram.Save(dataDir, SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **أشكال التخطيط في نمط المخطط الانسيابي**
 مع أنواع معينة من الرسومات المتصلة ، مثل المخططات الانسيابية والرسومات التخطيطية للشبكة ، يمكنك استخدام ملحق**أشكال التخطيط** ميزة لوضع الأشكال تلقائيًا. يعد تحديد المواقع تلقائيًا أسرع من سحب كل شكل يدويًا إلى موقع جديد.

على سبيل المثال ، إذا كنت تقوم بتحديث مخطط انسيابي كبير لتضمين عملية جديدة ، فيمكنك إضافة الأشكال التي تشكل العملية وتوصيلها ، ثم استخدام ميزة التخطيط لتخطيط الرسم المحدث تلقائيًا.

 طريقة Layout ، المكشوفة بواسطة ملف[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) تخطيطات الفصل للأشكال و / أو إعادة توجيه الموصلات على جميع صفحات diagram. هذه الطريقة تقبل ملف[خيارات التخطيط](https://reference.aspose.com/diagram/net/aspose.diagram.autolayout/layoutoptions)الكائن كحجة. استخدم الخصائص المختلفة المعروضة بواسطة فئة LayoutOptions لتخطيط الأشكال تلقائيًا.

توضح الصورة أدناه diagram الذي تم تحميله بواسطة مقتطفات التعليمات البرمجية في هذه المقالة ، قبل تطبيق التخطيط التلقائي. توضح مقتطفات التعليمات البرمجية كيفية التقديم[تخطيطات مخطط انسيابي](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) و[تخطيطات الشجرة المدمجة](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/).

**المصدر diagram.**

![ما يجب القيام به: image_بديل_نص](create-update-layout-and-auto-fit-shapes_1.png)

تأخذ مقتطفات التعليمات البرمجية في هذه المقالة المصدر diagram وتطبق عدة أنواع من التخطيط التلقائي عليها ، مع حفظ كل منها في ملف منفصل.

|<p>**تخطيط الأشكال من الأسفل إلى الأعلى** </p><p>![ما يجب القيام به: image_بديل_نص](create-update-layout-and-auto-fit-shapes_2.png)</p>|<p>**تخطيط الأشكال من أعلى إلى أسفل** </p><p>![ما يجب القيام به: image_بديل_نص](create-update-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**تخطيط الأشكال من اليسار إلى اليمين** </p><p>![ما يجب القيام به: image_بديل_نص](create-update-layout-and-auto-fit-shapes_4.png)</p>|<p>**تخطيط الأشكال من اليمين إلى اليسار** </p><p>![ما يجب القيام به: image_بديل_نص](create-update-layout-and-auto-fit-shapes_5.png)</p>|
لتخطيط الأشكال في نمط المخطط الانسيابي:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم بإنشاء مثيل لفئة LayoutOptions وقم بتعيين الخصائص ذات الصلة بنمط المخطط الانسيابي.
1. قم باستدعاء أسلوب تخطيط الفئة Diagram عن طريق تمرير LayoutOptions.
1. اتصل بـ Diagram class 'طريقة Save لكتابة رسم Visio.
### **عينة برمجة نمط المخطط الانسيابي**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load an existing Visio diagram
string fileName = "LayOutShapesInFlowchartStyle.vdx";
Diagram diagram = new Diagram(dataDir + fileName);

// Set layout options 
LayoutOptions flowChartOptions = new LayoutOptions();
flowChartOptions.LayoutStyle = LayoutStyle.FlowChart;
flowChartOptions.SpaceShapes = 1f;
flowChartOptions.EnlargePage = true;

// Set layout direction as BottomToTop and then save
flowChartOptions.Direction = LayoutDirection.BottomToTop;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_btm_top_out.vdx", SaveFileFormat.VDX);

// Set layout direction as TopToBottom and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.Direction = LayoutDirection.TopToBottom;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_top_btm_out.vdx", SaveFileFormat.VDX);

// Set layout direction as LeftToRight and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.Direction = LayoutDirection.LeftToRight;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_left_right_out.vdx", SaveFileFormat.VDX);

// Set layout direction as RightToLeft and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.Direction = LayoutDirection.RightToLeft;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_right_left_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
### **تخطيط الأشكال في نمط الشجرة المضغوطة**
 يحاول نمط تخطيط الشجرة المضغوط بناء هيكل شجرة. يستخدم نفس ملف الإدخال مثل ملف[المثال أعلاه](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/)ويحفظ في العديد من أنماط الأشجار المدمجة المختلفة.

|<p>**تخطيط شجرة مضغوط - لأسفل ولليمين** </p><p>![ما يجب القيام به: image_بديل_نص](create-update-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**تخطيط شجرة مضغوط - لأسفل ولليسار** </p><p>![ما يجب القيام به: image_بديل_نص](create-update-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**تخطيط شجرة مضغوط - لليمين ولأسفل** </p><p>![ما يجب القيام به: image_بديل_نص](create-update-layout-and-auto-fit-shapes_8.png)</p>|<p>**تخطيط شجرة مضغوط - لليسار ولأسفل** </p><p>![ما يجب القيام به: image_بديل_نص](create-update-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
لتخطيط الأشكال في نمط الشجرة المدمجة:

1.  قم بإنشاء مثيل لـ[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) صف دراسي.
1. قم بإنشاء مثيل لفئة LayoutOptions وقم بتعيين خصائص نمط الشجرة المدمجة.
1. قم باستدعاء أسلوب تخطيط الفئة Diagram عن طريق تمرير LayoutOptions.
1. قم باستدعاء الأسلوب Save للفئة Diagram لكتابة ملف Visio.
#### **عينة برمجة نمط الشجرة المدمجة**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

string fileName = "LayOutShapesInCompactTreeStyle.vdx";
// Load an existing Visio diagram
Diagram diagram = new Diagram(dataDir + fileName);

// Set layout options 
LayoutOptions compactTreeOptions = new LayoutOptions();
compactTreeOptions.LayoutStyle = LayoutStyle.CompactTree;
compactTreeOptions.EnlargePage = true;

// Set layout direction as DownThenRight and then save
compactTreeOptions.Direction = LayoutDirection.DownThenRight;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_down_right.vdx", SaveFileFormat.VDX);

// Set layout direction as DownThenLeft and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.Direction = LayoutDirection.DownThenLeft;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_down_left.vdx", SaveFileFormat.VDX);

// Set layout direction as RightThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.Direction = LayoutDirection.RightThenDown;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_right_down.vdx", SaveFileFormat.VDX);

// Set layout direction as LeftThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.Direction = LayoutDirection.LeftThenDown;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_left_down.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
## **احتواء تلقائي Visio Diagram**
 Aspose.Diagram API يدعم التركيب التلقائي للرسم Visio. تساعد عملية الميزة هذه على إحضار الأشكال الخارجية داخل حدود الصفحة Visio. Aspose.Diagram for .NET API لديه[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) فئة تمثل رسم Visio. ال[مخطط حفظ الخيارات](https://reference.aspose.com/diagram/net/aspose.diagram.saving/diagramsaveoptions) تعرض الفئة خاصية AutoFitPageToDrawingContent لتلائم الرسم Visio تلقائيًا.

هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. قم بإنشاء كائن من فئة DiagramSaveOptions وتمرير تنسيق الملف الناتج.
1. قم بتعيين خاصية AutoFitPageToDrawingContent للكائن DiagramSaveOptions.
1. استدعاء طريقة حفظ لكائن الفئة Diagram وأيضا تمرير مسار الملف الكامل وكائن DiagramSaveOptions.
### **عينة البرمجة الملائمة التلقائية**
يوضح رمز المثال التالي كيفية احتواء الأشكال تلقائيًا في Visio diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "BFlowcht.vsdx");

// Use saving options
DiagramSaveOptions options = new DiagramSaveOptions(SaveFileFormat.VSDX);
// Set Auto fit page property
options.AutoFitPageToDrawingContent = true;

// Save Visio diagram
diagram.Save(dataDir + "AutoFitShapesInVisio_out.vsdx", options);

{{< /highlight >}}
```
## **العمل مع مشروع VBA**
### **تعديل كود وحدة VBA في Visio Diagram**
 توضح هذه المقالة كيفية تعديل رمز وحدة VBA تلقائيًا باستخدام Aspose.Diagram for .NET. لقد أضفنا[VbaModule](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModule), [مجموعة VbaModuleCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModuleCollection), [VbaProject](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProject), [VbaProjectReference](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReference) و[VbaProjectReferenceCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReferenceCollection) الطبقات. تساعد هذه الفئات في التحكم في مشروع VBA. يمكن للمطورين استخراج وتعديل رمز الوحدة النمطية لـ VBA.
### **تعديل نموذج برمجة رمز الوحدة النمطية لـ VBA**
الرجاء التحقق من مثال هذا الرمز:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load an existing Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdm", LoadFileFormat.VSDM);
// Extract VBA project
Aspose.Diagram.Vba.VbaProject v = diagram.VbaProject;
// Iterate through the modules and modify VBA module code
foreach (VbaModule module in diagram.VbaProject.Modules)
{
    string code = module.Codes;
    if (code.Contains("This is test message."))
        code = code.Replace("This is test message.", "This is Aspose.Diagram message.");
    module.Codes = code;
}
// Save the Visio diagram
diagram.Save(dataDir + "ModifyVBAModule_out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}
```
### **قم بإزالة كافة وحدات الماكرو من Visio Diagram**
 Aspose.Diagram for .NET يسمح للمطورين بإزالة كافة وحدات الماكرو من Visio diagram.[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class ، تسمح لك بإزالة كافة وحدات الماكرو من الرسم Visio.
### **قم بإزالة كافة نماذج برمجة وحدات الماكرو**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Remove all macros
diagram.VbProjectData = null;

// Save diagram
diagram.Save(dataDir + "RemoveMacrosFromVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **إنشاء Diagram جديد مع VSTO**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)يتيح للمطورين إنشاء مخططات Microsoft Office Visio والعمل معها ودمج الميزات في تطبيقات البرامج الخاصة بهم. هناك طرق أخرى للعمل مع Visio من الملفات ، والأكثر شيوعًا هو Microsoft Automation. لسوء الحظ ، هذا له بعض القيود. Aspose.Diagram قوي وسريع ويعمل بشكل مستقل دون تثبيت Microsoft Office.

 توضح مقالة الترحيل هذه كيفية الاستخدام أولاً[VSTO](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) وثم[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) لإنشاء diagram جديد وإضافة بعض الأشكال إليه. ستلاحظ أن كود Aspose.Diagram أقصر من كود VSTO. لا تتردد في استخدام الكود كأساس لتطويرك الخاص وتعزيزه لتلبية احتياجاتك. يتيح لك VSTO البرمجة باستخدام ملفات Microsoft Visio. لإنشاء diagram جديد:

1. قم بتكوين عنصر تطبيق Visio.
1. جعل كائن التطبيق غير مرئي.
1. قم بإنشاء diagram فارغًا.
1. أضف الأشكال من Visio الماجستير (الإستنسل).
1. احفظ الملف باسم VDX.
### **قم بإنشاء Diagram جديد باستخدام نموذج برمجة VSTO**
{{% alert color="primary" %}}

باستخدام Visio = Microsoft.Office.Interop.Visio ؛
الواردات Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}


**مثال:**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

Visio.Application vdxApp = null;
Visio.Document vdxDoc = null;
try
{
    // Create Visio Application Object
    vdxApp = new Visio.Application();

    // Make Visio Application Invisible
    vdxApp.Visible = false;

    // Create a new diagram
    vdxDoc = vdxApp.Documents.Add("");

    // Load Visio Stencil
    Visio.Documents visioDocs = vdxApp.Documents;
    Visio.Document visioStencil = visioDocs.OpenEx("Basic Shapes.vss",
        (short)Microsoft.Office.Interop.Visio.VisOpenSaveArgs.visOpenHidden);

    // Set active page
    Visio.Page visioPage = vdxApp.ActivePage;

    // Add a new rectangle shape
    Visio.Master visioRectMaster = visioStencil.Masters.get_ItemU(@"Rectangle");
    Visio.Shape visioRectShape = visioPage.Drop(visioRectMaster, 4.25, 5.5);
    visioRectShape.Text = @"Rectangle text.";

    // Add a new star shape
    Visio.Master visioStarMaster = visioStencil.Masters.get_ItemU(@"Star 7");
    Visio.Shape visioStarShape = visioPage.Drop(visioStarMaster, 2.0, 5.5);
    visioStarShape.Text = @"Star text.";

    // Add a new hexagon shape
    Visio.Master visioHexagonMaster = visioStencil.Masters.get_ItemU(@"Hexagon");
    Visio.Shape visioHexagonShape = visioPage.Drop(visioHexagonMaster, 7.0, 5.5);
    visioHexagonShape.Text = @"Hexagon text.";


    // Save diagram as VDX
    vdxDoc.SaveAs(dataDir + "CreatingDiagramWithVSTO_out.vdx");
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message + "\nThis example will only work if you apply a valid Aspose License. You can purchase full license or get 30 day temporary license from http:// Www.aspose.com/purchase/default.aspx.");
}
            

{{< /highlight >}}
```
## **إنشاء Diagram جديد مع Aspose.Diagram for .NET**
باستخدام Aspose.Diagram API ، لا يحتاج المطورون إلى تثبيت Microsoft Office Visio على الجهاز ، ويمكنهم العمل بشكل مستقل عن Microsoft Office Automation.

لإنشاء diagram جديد:

1. قم بإنشاء diagram فارغًا.
1. أضف الأشكال من Visio الماجستير (الإستنسل).
1. احفظ الملف باسم VDX.
### **Diagram جديد مع عينة برمجة Aspose.Diagram for .NET**
{{% alert color="primary" %}}

باستخدام Aspose.Diagram ؛
الواردات Aspose.Diagram

{{% /alert %}}

مثال:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

// Create a new diagram
Diagram diagram = new Diagram(dataDir + "Basic Shapes.vss");

// Add a new rectangle shape
long shapeId = diagram.AddShape(4.25, 5.5, 2, 1, @"Rectangle", 0);
Shape shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Rectangle text."));

// Add a new star shape
shapeId = diagram.AddShape(2.0, 5.5, 2, 2, @"Star 7", 0);
shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Star text."));

// Add a new hexagon shape
shapeId = diagram.AddShape(7.0, 5.5, 2, 2, @"Hexagon", 0);
shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Hexagon text."));

// Save the new diagram
diagram.Save(dataDir + "CreatingDiagramWithAspose_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
## **تحديث خصائص الشكل**
 عند العمل باستخدام الرسوم التخطيطية Microsoft Visio ، يمكن للمستخدمين تحديث سمات الشكل بما في ذلك النص والنمط والموضع والارتفاع والعرض. بصفتك مطور برامج يعمل مع ملفات Visio ، سيُطلب منك القيام بذلك برمجيًا. والخبر السار هو أنه من الممكن ، إما باستخدام آليات البرمجة مع Visio الملفات التي يوفرها Microsoft أو VSTO أو باستخدام[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 يوضح الموضوع أدناه كيفية الاستخدام[VSTO](https://products.aspose.com/diagram/net/) و[Aspose.Diagram](https://products.aspose.com/diagram/net/) لتحديث خصائص الشكل. توضح مقتطفات التعليمات البرمجية أدناه كيفية تحديث خصائص الشكل لـ VSTO و Aspose.Diagram for .NET. لا تتردد في استخدام الكود وتطبيقه على حالتك الخاصة.
### **تحديث خصائص الشكل باستخدام VSTO**
يتيح لك VSTO البرمجة باستخدام ملفات Microsoft Visio. لتحديث خصائص الشكل:

1. قم بتكوين عنصر تطبيق Visio.
1. جعل كائن التطبيق غير مرئي.
1. افتح ملف Visio VSD موجود.
1. ابحث عن الشكل المطلوب.
1. قم بتحديث خصائص الشكل (النص ونمط النص والموضع والحجم).
1. احفظ الملف باسم VDX.
#### **تحديث خصائص الشكل بنموذج برمجة VSTO**
{{% alert color="primary" %}}

باستخدام Visio = Microsoft.Office.Interop.Visio ؛
الواردات Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}

**مثال:**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

Visio.Application vsdApp = null;
Visio.Document vsdDoc = null;
try
{
    // Create Visio Application Object
    vsdApp = new Visio.Application();

    // Make Visio Application Invisible
    vsdApp.Visible = false;

    // Create a document object and load a diagram
    vsdDoc = vsdApp.Documents.Open(dataDir + "Drawing1.vsd");

    // Create page object to get required page
    Visio.Page page = vsdApp.ActivePage;

    // Create shape object to get required shape
    Visio.Shape shape = page.Shapes["Process1"];

    // Set shape text and text style
    shape.Text = "Hello World";
    shape.TextStyle = "CustomStyle1";

    // Set shape's position
    shape.get_Cells("PinX").ResultIU = 5;
    shape.get_Cells("PinY").ResultIU = 5;

    // Set shape's height and width
    shape.get_Cells("Height").ResultIU = 2;
    shape.get_Cells("Width").ResultIU = 3;

    // Save file as VDX
    vsdDoc.SaveAs(dataDir + "Drawing1.vdx");
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message + "\nThis example will only work if you apply a valid Aspose License. You can purchase full license or get 30 day temporary license from http:// Www.aspose.com/purchase/default.aspx.");
}           

{{< /highlight >}}
```
### **تحديث خصائص الشكل مع Aspose.Diagram for .NET**
باستخدام Aspose.Diagram API ، لا يحتاج المطورون إلى Microsoft Office Visio على الجهاز ، ويمكنهم العمل بشكل مستقل عن Microsoft Office Automation.

لتحديث خصائص الشكل باستخدام Aspose.Diagram for .NET:

1. افتح ملف Visio VSD موجود.
1. ابحث عن الشكل المطلوب.
1. قم بتحديث خصائص الشكل (النص ونمط النص والموضع والحجم).
1. احفظ الملف باسم VDX.
#### **تحديث خصائص الشكل باستخدام عينة البرمجة Aspose.Diagram for .NET**
{{% alert color="primary" %}}

باستخدام Aspose.Diagram ؛
الواردات Aspose.Diagram

{{% /alert %}}

**مثال:**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
try
{
    // The path to the documents directory.
    string dataDir = RunExamples.GetDataDir_KnowledgeBase();

    // Save the uploaded file as PDF
    Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");

    // Find a particular shape and update its properties
    foreach (Aspose.Diagram.Shape shape in diagram.Pages[0].Shapes)
    {
        if (shape.Name.ToLower() == "process1")
        {
            shape.Text.Value.Clear();
            shape.Text.Value.Add(new Txt("Hello World"));

            // Find custom style sheet and set as shape's text style
            foreach (StyleSheet styleSheet in diagram.StyleSheets)
            {
                if (styleSheet.Name == "CustomStyle1")
                {
                    shape.TextStyle = styleSheet;
                }
            }

            // Set horizontal and vertical position of the shape
            shape.XForm.PinX.Value = 5;
            shape.XForm.PinY.Value = 5;

            // Set height and width of the shape
            shape.XForm.Height.Value = 2;
            shape.XForm.Width.Value = 3;
        }
    }

    // Save shape as VDX
    diagram.Save(dataDir + "UpdateShapePropsWithAspose_out.vdx", SaveFileFormat.VDX);
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message);
}

{{< /highlight >}}
```
