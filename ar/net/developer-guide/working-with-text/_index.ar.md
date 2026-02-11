---
title: العمل مع النص
type: docs
weight: 90
url: /ar/net/working-with-text/
description: يوضح هذا القسم كيفية إدراج شكل نص أو تحديث نص الشكل باستخدام Aspose.Diagram.
---
## **أدخل شكل نص في صفحة Visio**
 Aspose.Diagram API يتيح للمطورين إدراج شكل نص في أي مكان في صفحة Visio. لتحقيق ذلك ، فإن أسلوب AddText الخاص ببرنامج[صفحة](http://www.aspose.com/api/net/diagram/aspose.diagram/page) يأخذ الفصل معلمات PinX و PinY والعرض والارتفاع والنص.
### **أدخل نموذجًا لبرمجة شكل النص**
يضيف جزء الكود التالي شكل نص في Visio diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Create a new diagram
Diagram diagram = new Diagram();
// Set parameters and add text to a Visio page
double PinX = 1, PinY = 1, Width = 1, Height = 1;                  
diagram.Pages[0].AddText(PinX, PinY, Width, Height, "Test text");
// Save diagram 
diagram.Save(dataDir + "InsertTextShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **تحديث Visio شكل النص**
 إلى جانب[إنشاء الرسوم البيانية](/diagram/ar/net/load-or-create-a-visio-drawing/) ، Aspose.Diagram for .NET يتيح لك العمل مع الأشكال بطرق مختلفة. تتناول هذه المقالة كيفية الوصول إلى النص في الأشكال وتحديثه. خاصية Text ، المكشوفة بواسطة ملف[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) فئة ، تدعم الكائن Aspose.Diagram.Text. يمكن استخدام الخاصية لاسترداد نص الشكل أو تحديثه. عملية تحديث نص الشكل مباشرة:

1. قم بتحميل diagram.
1. ابحث عن شكل معين.
1. قم بتعيين النص الجديد.
1. احفظ diagram.
### **تحديث نموذج برمجة نص الشكل**
يقوم الجزء التالي من التعليمات البرمجية بتحديث نص الشكل. يتم تحديد الأشكال من خلال معرفاتهم. تبحث مقاطع التعليمات البرمجية أدناه عن شكل يسمى العملية ومع المعرف 1 وتغيير نصه.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "UpdateShapeText.vsd");
// Get page by name
Page page = diagram.Pages.GetPage("Flow 1");
// Find a particular shape and update its text
foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.NameU.ToLower() == "process" && shape.ID == 1)
    {
        shape.Text.Value.Clear();
        shape.Text.Value.Add(new Txt("New Text"));
    }
}
// Save diagram
diagram.Save(dataDir + "UpdateShapeText_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

## **قم بتطبيق ورقة أنماط مدمجة أو مخصصة على شكل Visio**
تخزن أوراق الأنماط Microsoft Visio معلومات التنسيق التي يمكن تطبيقها على الأشكال للحصول على مظهر وأسلوب عرض متسقين. Aspose.Diagram for .NET يسمح لك بتطبيق أوراق الأنماط من داخل التطبيق.

 خصائص TextStyle و FillStyle و LineStyle المعروضة بواسطة ملف[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) فئة دعم[Aspose.Diagram.StyleSheet](http://www.aspose.com/api/net/diagram/aspose.diagram/stylesheet) هدف. يمكن استخدام الخاصية لاسترداد معلومات النمط وتطبيق أنماط مخصصة للنص والخط والتعبئة على diagram.
### **الأنماط المخصصة في Microsoft Visio**
لتطبيق أنماط مخصصة على الأشكال في Microsoft Visio:

1. افتح diagram في Microsoft Visio.
1.  يختار**تحديد الأنماط** من**شكل** القائمة (Visio 2007) ، أو انقر بزر الماوس الأيمن**الأنماط** في ال**مستكشف الرسم** نافذة ، وحدد**تحديد الأنماط** (Visio 2010).
1.  في ال**تحديد الأنماط** في مربع الحوار ، اكتب اسمًا جديدًا لورقة الأنماط المخصصة الخاصة بك. على سبيل المثال ، CustomStyle1.
1.  انقر على**نص**, **خط** و**يملأ** لتعيين أنماط النص والخط والتعبئة على التوالي.
1.  انقر**نعم**.

بعد تحديد أوراق الأنماط المخصصة في Microsoft Visio ، استخدم الكود التالي في تطبيق .NET لتطبيق الأنماط المخصصة على الأشكال الخاصة بك. لاحظ أن نماذج التعليمات البرمجية أدناه تستدعي ورقة الأنماط المخصصة المحددة أعلاه: تحتاج إلى معرفة اسم وموقع الورقة التي تقوم بتطبيقها. لتطبيق الأنماط المخصصة برمجيًا:

1. قم بتحميل diagram.
1. ابحث عن الشكل الذي تريد تطبيق النمط عليه.
1. قم بتحميل ورقة الأنماط.
1. تطبيق الأنماط.
1. احفظ diagram.
#### **تطبيق نموذج برمجة أنماط مخصصة**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Load diagram
Diagram vsdDiagram = new Diagram(dataDir + "ApplyCustomStyleSheets.vsd");
// Get page by name
Page page = vsdDiagram.Pages.GetPage("Flow 1");

Shape sourceShape = null;
// Find the shape to apply the style
foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.Name == "Process")
    {
        sourceShape = shape;
        break;
    }
}

StyleSheet customStyleSheet = null;

// Find the required style sheet
foreach (StyleSheet styleSheet in vsdDiagram.StyleSheets)
{
    if (styleSheet.Name == "Basic")
    {
        customStyleSheet = styleSheet;
        break;
    }
}

if (sourceShape != null && customStyleSheet != null)
{
    // Apply text style
    sourceShape.TextStyle = customStyleSheet;
    // Apply fill style
    sourceShape.FillStyle = customStyleSheet;
    // Apply line style
    sourceShape.LineStyle = customStyleSheet;
}

// Save changed diagram as VDX
vsdDiagram.Save(dataDir + "ApplyCustomStyleSheets_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

## **قم بتطبيق نمط مختلف على كل قيمة نصية لشكل**
 إلى جانب[إنشاء الرسوم البيانية](/diagram/ar/net/load-or-create-a-visio-drawing/)، Aspose.Diagram for .NET يتيح لك العمل مع الأشكال بطرق مختلفة. تساعد هذه المقالة في إضافة قيم نصية متعددة إلى شكل وتطبيق نمط مختلف على كل قيمة نصية.

{{% alert color="primary" %}} 

يحتوي عنصر الشكل على عنصر يسمى Text ، والذي يحتوي على أحرف النص والعناصر الخاصة (cp و pp و tp و fld) التي تحدد نهاية تشغيل واحد وبداية تشغيل التالي. يحتوي Char Element على سمات التنسيق لنص الشكل ، مثل الخط واللون ونمط النص والحالة والموقع بالنسبة إلى الخط الأساسي وحجم النقطة.

{{% /alert %}} 
### **إضافة نص الشكل والأنماط**

|**المدخلات diagram**|
|:- |
|![ما يجب القيام به: image_بديل_نص](working-with-text_1.png)|


|**Diagram بعد إضافة قيم نصية مختلفة لشكل بنمط مختلف لكل قيمة نصية**|
|:- |
|![ما يجب القيام به: image_بديل_نص](working-with-text_2.png)|
#### **إضافة نموذج برمجة نص وأنماط**
تضيف قطعة الكود التالية نصًا للشكل وأنماطًا مختلفة.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(1);
// Clear shape text values and chars
shape.Text.Value.Clear();
shape.Chars.Clear();

// Mark character run and add text
shape.Text.Value.Add(new Cp(0));
shape.Text.Value.Add(new Txt("TextStyle_Regular\n"));
shape.Text.Value.Add(new Cp(1));
shape.Text.Value.Add(new Txt("TextStyle_Bold_Italic\n"));
shape.Text.Value.Add(new Cp(2));
shape.Text.Value.Add(new Txt("TextStyle_Underline_Italic\n"));
shape.Text.Value.Add(new Cp(3));
shape.Text.Value.Add(new Txt("TextStyle_Bold_Italic_Underline"));

// Add formatting characters
shape.Chars.Add(new Aspose.Diagram.Char());
shape.Chars.Add(new Aspose.Diagram.Char());
shape.Chars.Add(new Aspose.Diagram.Char());
shape.Chars.Add(new Aspose.Diagram.Char());

// Set properties e.g. color, font, size and style etc.
shape.Chars[0].IX = 0;
shape.Chars[0].Color.Value = "#FF0000";
shape.Chars[0].Font.Value = 4;
shape.Chars[0].Size.Value = 0.22;
shape.Chars[0].Style.Value = StyleValue.Undefined;

// Set properties e.g. color, font, size and style etc.
shape.Chars[1].IX = 1;
shape.Chars[1].Color.Value = "#FF00FF";
shape.Chars[1].Font.Value = 4;
shape.Chars[1].Size.Value = 0.22;
shape.Chars[1].Style.Value = StyleValue.Bold | StyleValue.Italic;

// Set properties e.g. color, font, size and style etc.
shape.Chars[2].IX = 2;
shape.Chars[2].Color.Value = "#00FF00";
shape.Chars[2].Font.Value = 4;
shape.Chars[2].Size.Value = 0.22;
shape.Chars[2].Style.Value = StyleValue.Underline | StyleValue.Italic;

// Set properties e.g. color, font, size and style etc.
shape.Chars[3].IX = 3;
shape.Chars[3].Color.Value = "#3333FF";
shape.Chars[3].Font.Value = 4;
shape.Chars[3].Size.Value = 0.22;
shape.Chars[3].Style.Value = StyleValue.Bold | StyleValue.Italic | StyleValue.Underline;
// Save diagram
diagram.Save(dataDir + "ApplyFontOnText_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **البحث عن نص الشكل واستبداله**
 ال[رسالة قصيرة](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) يسمح لك Class بتعديل نص الشكل. طريقة الاستبدال ، المكشوفة بواسطة[رسالة قصيرة](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) فئة ، دعم تغيير نص الشكل.
تبحث أمثلة التعليمات البرمجية في هذه المقالة عن نص الشكل على الصفحة واستبداله.

|**المدخلات diagram**|
|:- |
|![ما يجب القيام به: image_بديل_نص](working-with-text_3.png)|


|**diagram بعد تحرير الشكل**|
|:- |
|![ما يجب القيام به: image_بديل_نص](working-with-text_4.png)|
عملية تغيير نص الشكل:

1. قم بتحميل diagram.
1. ابحث عن نص معين للشكل.
1. استبدل نص هذا الشكل
1. احفظ diagram.
### **بحث واستبدال عينة برمجة نصية**
توضح مقتطفات التعليمات البرمجية أدناه كيفية تعديل نص الشكل. تتكرر الشفرة عبر أشكال الصفحة.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Prepare a collection old and new text
Dictionary<string, string> replacements = new Dictionary<string, string>();
replacements.Add("[[CompanyName]]", "Research Society of XYZ");
replacements.Add("[[EmployeeName]]", "James Bond");
replacements.Add("[[SubjectTitle]]", "The affect of the internet on social behavior in the industrialize world");
replacements.Add("[[TimePeriod]]", DateTime.Now.AddYears(-1).ToString("dd/MMMM/yyyy") + " -- " + DateTime.Now.ToString("dd/MMMM/yyyy"));
replacements.Add("[[SubmissionDate]]", DateTime.Now.AddDays(-7).ToString("dd/MMMM/yyyy"));
replacements.Add("[[AmountReq]]", "$100,000");
replacements.Add("[[DateApproved]]", DateTime.Now.AddDays(1).ToString("dd/MMMM/yyyy"));

// Load diagram
Diagram diagram = new Diagram(dataDir + "FindReplaceText.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");

// Iterate through the shapes of a page
foreach (Shape shape in page.Shapes)
{
    foreach (KeyValuePair<string, string> kvp in replacements)
    {
        foreach (FormatTxt txt in shape.Text.Value)
        {
            Txt tx = txt as Txt;
            if (tx != null && tx.Text.Contains(kvp.Key))
            {
                // Find and replace text of a shape
                tx.Text = tx.Text.Replace(kvp.Key, kvp.Value);
            }
        }
    }
}
// Save the diagram
diagram.Save(dataDir + "FindAndReplaceShapeText_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **استخراج نص عادي من Visio Diagram صفحة**
Aspose.Diagram API يسمح للمطورين باستخراج نص عادي من صفحة Visio diagram. يمكنهم أيضًا تكرار الصفحات Visio diagram لتغطية النص Visio diagram بالكامل.

 Microsoft Office Visio يقوم باضافة النص الى الاشكال. ال[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) تحتوي الفئة على عنصر يسمى Text ، والذي يحتوي على أحرف النص والعناصر الخاصة (cp ، و pp ، و tp ، و fld) التي تحدد نهاية تشغيل واحد وبداية تشغيل ما يليه.
### **استخراج عينة برمجة نص عادي**
يتكرر جزء الكود التالي من خلال أشكال الصفحة Visio ويقوم بتصفية النص العادي بدون معلومات التنسيق.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
static string text = "";
public static void Run()
{
    // The path to the documents directory.
    string dataDir = RunExamples.GetDataDir_ShapeText();
    // Load diagram
    Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

    // Get Visio diagram page
    Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

    // Iterate through the shapes
    foreach (Aspose.Diagram.Shape shape in page.Shapes)
    {
        // Extract plain text from the shape
        GetShapeText(shape);
    }
    // Display extracted text
    Console.WriteLine(text);
}
private static void GetShapeText(Aspose.Diagram.Shape shape)
{
    // Filter shape text
    if (shape.Text.Value.Text != "")
        text += Regex.Replace(shape.Text.Value.Text, "\\<.*?>", "");

    // For image shapes
    if (shape.Type == TypeValue.Foreign)
        text += (shape.Name);

    // For group shapes
    if (shape.Type == TypeValue.Group)
        foreach (Aspose.Diagram.Shape subshape in shape.Shapes)
        {
            GetShapeText(subshape);
        }
}

{{< /highlight >}}

