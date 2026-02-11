---
title: إضافة بيانات الشكل واستردادها ونسخها وقراءتها Visio
type: docs
weight: 10
url: /ar/net/add-retrieve-copy-and-read-visio-shape-data/
description: يشرح هذا القسم كيفية إضافة شكل أو تعيين خاصية الشكل أو نسخ شكل باستخدام Aspose.Diagram.
---
## **إضافة شكل جديد في Visio**
Aspose.Diagram for .NET يسمح لك بمعالجة Microsoft Visio المخططات بطرق مختلفة. أحد الأشياء التي يمكنك القيام بها هو إضافة أشكال جديدة إلى الرسوم التخطيطية. يتيح لك Aspose.Diagram for .NET إضافة شكل جديد إلى diagram. يمكن أيضًا تخصيص الشكل المضاف باستخدام Aspose.Diagram for .NET.

يصف هذا الموضوع كيفية إضافة شكل مستطيل جديد إلى diagram.

استخدم Aspose.Diagram for .NET API لإنشاء أشكال جديدة ثم قم بإضافة هذه الأشكال إلى مجموعة أشكال diagram.

لإضافة شكل جديد:

1. **ابحث عن الصفحة** - يحتوي كل Visio diagram على مجموعة من الصفحات. يمكن للمطورين استرداد الصفحة حسب معرّف الصفحة أو الاسم وتخزين الصفحة المطلوبة في ملف[صفحة](http://www.aspose.com/api/net/diagram/aspose.diagram/page)كائن فئة.
1. **أضف المطلوب الرئيسي للشكل** - يحتوي كل Visio diagram على مجموعة من الأساتذة. يمكن للمطورين إضافة رئيسي (بواسطة المعرف أو الاسم) من ملف الاستنسل الموجود (عن طريق المسار المباشر أو دفق الملف).
1. **أضف شكلاً في Visio diagram** - يمكن للمطورين وضع شكل جديد في Visio diagram حسب فهرس الصفحة (يبدأ من 0) ، الاسم الرئيسي ، PinX ، PinY ، الارتفاع (اختياري) والعرض (اختياري).
1. **تعيين خصائص الشكل** - تقوم طريقة AddShape للفئة Diagram بإرجاع معرف الشكل. يمكن للمطورين استرداد الشكل من diagram Visio باستخدام هذا المعرف ، ثم تعيين خصائصه ، مثل اللون والموضع والمحاذاة والنص.

|<p>**المدخلات diagram** </p><p>![ما يجب القيام به: image_بديل_نص](add-retrieve-copy-and-read-visio-shape-data_1.png)</p>|<p>**diagram مع إضافة الشكل** </p><p>![ما يجب القيام به: image_بديل_نص](add-retrieve-copy-and-read-visio-shape-data_2.png)</p>|
|:- |:- |
### **إضافة عينة البرمجة**
يوضح مقتطف الشفرة أدناه كيفية القيام بكل خطوة.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-2");

// Add master with stencil file path and master name
string masterName = "Rectangle";
diagram.AddMaster(dataDir + "Basic Shapes.vss", masterName);
            
// Page indexing starts from 0
int PageIndex = 1;
double width = 2, height = 2, pinX = 4.25, pinY = 4.5;
// Add a new rectangle shape
long rectangleId = diagram.AddShape(pinX, pinY, width, height, masterName, PageIndex);
            
// Set shape properties 
Shape rectangle = page.Shapes.GetShape(rectangleId);
rectangle.XForm.PinX.Value = 5;
rectangle.XForm.PinY.Value = 5;
rectangle.Type = TypeValue.Shape;
rectangle.Text.Value.Add(new Txt("Aspose Diagram"));
rectangle.TextStyle = diagram.StyleSheets[3];
rectangle.Line.LineColor.Value = "#ff0000";
rectangle.Line.LineWeight.Value = 0.03;
rectangle.Line.Rounding.Value = 0.1;
rectangle.Fill.FillBkgnd.Value = "#ff00ff";
rectangle.Fill.FillForegnd.Value = "#ebf8df";

diagram.Save(dataDir + "AddShape_out.vsdx", SaveFileFormat.VSDX);
Console.WriteLine("Shape has been added.");

{{< /highlight >}}


{{% alert color="primary" %}}

 نرحب باستفساراتكم واقتراحاتكم على[Aspose.Diagram المنتدى](https://forum.aspose.com/c/diagram/17). سوف نقوم بالرد على الفور.

{{% /alert %}}
## **استرجاع معلومات الشكل**
[العمل مع المخططات](/diagram/ar/net/working-with-diagrams/)يشرح كيفية إنشاء الرسوم البيانية وإضافة الأشكال والموصلات ، ثم كيفية استرداد المعلومات حول عناصر diagram مثل[الصفحات](/diagram/ar/net/retrieve-2c-get-2c-copy-and-insert-a-page/), [سادة](https://docs.aspose.com/diagram/net/working-with-masters/), [موصلات](/diagram/ar/net/retrieving-connector-information/) و[الخطوط](/diagram/ar/net/retrieving-font-information/). تبحث هذه المقالة في كيفية استرداد معلومات حول الأشكال في diagram.

كل شكل في diagram له معرف واسم. المعرف مهم عند البرمجة باستخدام Visio: إنه الطريقة الرئيسية للوصول إلى الشكل. يحتفظ كل شكل أيضًا بمعلومات حول العنصر الرئيسي (الاستنسل) الذي يتكون منه.

 أ[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) هو كائن في رسم Visio. تدعم خاصية الأشكال ، المكشوفة بواسطة فئة الصفحة ، مجموعة من Aspose.Diagram كائنات الشكل. يمكن استخدام الخاصية الأشكال لاسترداد معلومات حول الشكل.

في نافذة وحدة التحكم أدناه ، على سبيل المثال ، يمكنك مشاهدة إخراج المعلومات لـ diagram الذي يحتوي على أربعة أشكال: محطتي إنهاء وعملية وموصل ديناميكي. لكل منها معرف فريد بالإضافة إلى اسم الشكل الرئيسي (الاستنسل).

|**نافذة وحدة تحكم تعرض معلومات الشكل**|
|:- |
|![ما يجب القيام به: image_بديل_نص](add-retrieve-copy-and-read-visio-shape-data_3.png)|
لاسترداد معلومات الصفحة Visio:

1. يحمل diagram.
1. يقوم بإعداد حلقة foreach للتكرار خلال كل الأشكال الموجودة في diagram.
1. يعرض معلومات الشكل.
### **استرجاع عينة البرمجة**
تسترد قطعة الكود التالية معلومات الشكل من Visio diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load diagram
Diagram vsdDiagram = new Diagram(dataDir + "RetrieveShapeInfo.vsd");

foreach (Aspose.Diagram.Shape shape in vsdDiagram.Pages[0].Shapes)
{
    // Display information about the shapes
    Console.WriteLine("\nShape ID : " + shape.ID);
    Console.WriteLine("Name : " + shape.Name);
    Console.WriteLine("Master Shape : " + shape.Master.Name);
}

{{< /highlight >}}

## **نسخ الأشكال من Visio موجود**
Aspose.Diagram for .NET API يسمح للمطورين بنسخ الأشكال من صفحة المصدر Visio إلى صفحة Visio diagram الجديدة. كما يدعم نسخ أشكال المجموعة. توضح هذه المقالة كيفية نسخ كافة الأشكال من الصفحة diagram المصدر.

لنسخ الأشكال ، يجب على المطورين أيضًا نسخ نسق ورقة الصفحة والمصدر Visio المصدر للاحتفاظ بنمط تعبئة الشكل وخصائص التنسيق الأخرى.

هذا المثال يعمل على النحو التالي:

1. قم بتحميل المصدر Visio.
1. تهيئة Visio جديد
1. قم بإضافة الأساسيات والنُسق من المصدر Visio.
1. احصل على الصفحة من المصدر Visio.
1. انسخ ورقة الصفحة الخاصة بها إلى صفحة Visio الجديدة.
1. التكرار من خلال أشكال الصفحة Visio المصدر.
1. قم بتعيين معرفه الجديد وأضفه إلى صفحة Visio الجديدة.
1. احفظ Visio الجديد في التخزين المحلي.
### **عينة برمجة نسخ**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();
            
// Load a source Visio
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");
            
// Initialize a new Visio
Diagram newDiagram = new Diagram();

// Add all masters from the source Visio diagram
MasterCollection originalMasters = srcVisio.Masters;
foreach (Master master in originalMasters)
    newDiagram.AddMaster(srcVisio, master.Name);

// Get the page object from the original diagram
Aspose.Diagram.Page SrcPage = srcVisio.Pages.GetPage("Page-1");
// Copy themes from the source diagram
newDiagram.CopyTheme(srcVisio);
// Copy pagesheet of the source Visio page
newDiagram.Pages[0].PageSheet.Copy(SrcPage.PageSheet);

// Copy shapes from the source Visio page
foreach (Aspose.Diagram.Shape shape in SrcPage.Shapes)
{
    newDiagram.Pages[0].Shapes.Add(shape);
}
// Save the new Visio
newDiagram.Save(dataDir + "CopyShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


{{% alert color="primary" %}}

 نرحب باستفساراتكم واقتراحاتكم على[Aspose.Diagram المنتدى](https://forum.aspose.com/c/diagram/17). سوف نقوم بالرد على الفور.

{{% /alert %}}
## **انسخ شكل Visio إلى مثيل Shape آخر**
تأخذ طريقة النسخ الخاصة بفئة الشكل مثيل شكل للنسخ.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Shape newShape = new Shape();

// copy diagram

newShape.Copy(diagram.Pages[0].Shapes[0]);

newShape.ID = 3;

newShape.XForm.PinX.Value = 1;

newShape.XForm.PinY.Value = 1;

{{< /highlight >}}
## **قراءة Visio بيانات الشكل**
 مجموعة Props التي كشفها[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) فئة تدعم[Aspose.Diagram.Prop](http://www.aspose.com/api/net/diagram/aspose.diagram/prop) هدف. يمكن استخدام الخاصية لقراءة بيانات الشكل (الخصائص المخصصة).
### **قراءة كافة خصائص الشكل**
لتحديد الخصائص المخصصة في Microsoft Visio:

1. في diagram ، انقر بزر الماوس الأيمن فوق شكل.
1.  يختار**بيانات** ، ومن بعد**بيانات الشكل** من القائمة.
 يتم سرد أي خصائص موجودة في مربع الحوار.

|**بيانات الشكل ، كما هو موضح في Microsoft Visio.**|** |
|:- |:- |
|![ما يجب القيام به: image_بديل_نص](add-retrieve-copy-and-read-visio-shape-data_4.png)||


|**نافذة وحدة تحكم تعرض إخراج بيانات الشكل.**|** |
|:- |:- |
|![ما يجب القيام به: image_بديل_نص](add-retrieve-copy-and-read-visio-shape-data_5.png)||
#### **قراءة نموذج البرمجة**
تقرأ مقتطفات التعليمات البرمجية أدناه بيانات الشكل (الخصائص المخصصة).


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.Name == "Process1")
    {
        foreach (Prop property in shape.Props)
        {
            Console.WriteLine(property.Label.Value + ": " + property.Value.Val);
        }
        break;
    }
}

{{< /highlight >}}

### **اقرأ خاصية الشكل بالاسم**
يقرأ مقتطف الشفرة أدناه خاصية الشكل بالاسم (خاصية مخصصة).
#### **تمت قراءتها حسب نموذج برمجة الاسم**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.Name == "Process1")
    {
        Prop property = shape.Props.GetProp("Name1");
        Console.WriteLine(property.Label.Value + ": " + property.Value.Val);
    }
}

{{< /highlight >}}

### **اقرأ InheritProps of Shape**
يقرأ مقتطف الشفرة أدناه InheritProps لشكل.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    foreach (Aspose.Diagram.Prop prop in shape.InheritProps)
    {
        Console.WriteLine(prop.Name);
        Console.WriteLine(prop.Label.Value);
        Console.WriteLine(prop.Prompt.Value);
        Console.WriteLine(prop.Type.Value.ToString());
        Console.WriteLine(prop.Value.Val);
        Console.WriteLine(prop.Format.Value);
    }
}

{{< /highlight >}}

## **إضافة وتوصيل Visio الأشكال**
 Aspose.Diagram for .NET يسمح لك بإضافة أشكال مخصصة وربطها[الرسوم البيانية التي تقوم بإنشائها](https://products.aspose.com/diagram/net/).
### **إضافة وتوصيل الأشكال**
يوضح الكود الموجود في العينات أدناه كيفية:

1. قم بإنشاء diagram.
1. قم بإضافة الأشكال وتخصيصها (مستطيل ، نجمة ، مسدس).
1. قم بتوصيل الأشكال النجمية والسداسية بالمستطيل.
1. احفظ diagram.
#### **نموذج برمجة إضافة وتوصيل الأشكال**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_TechnicalArticles();

// Set license (you can add 10 shapes without setting a license)
// License lic = new License();
// Lic.SetLicense(dataDir + "Aspose.Total.lic");

// Load masters from any existing diagram, stencil or template
// And add in the new diagram
string visioStencil = dataDir + "AddConnectShapes.vss";

// Names of the masters present in the stencil
string rectangleMaster = @"Rectangle", starMaster = @"Star 7",
    hexagonMaster = @"Hexagon", connectorMaster = "Dynamic connector";

int pageNumber = 0;
double width = 2, height = 2, pinX = 4.25, pinY = 9.5;

// Create a new diagram
Diagram diagram = new Diagram(visioStencil);

// Add a new rectangle shape
long rectangleId = diagram.AddShape(
    pinX, pinY, width, height, rectangleMaster, pageNumber);

// Set the new shape's properties
Shape shape = diagram.Pages[pageNumber].Shapes.GetShape(rectangleId);
shape.Text.Value.Add(new Txt(@"Rectangle text."));
shape.Name = "Rectangle1";
shape.XForm.LocPinX.Ufe.F = "Width*0.5";
shape.XForm.LocPinY.Ufe.F = "Height*0.5";
shape.Line.LineColor.Value = "7";
shape.Line.LineWeight.Value = 0.03;
shape.Fill.FillBkgnd.Value = "1";
shape.Fill.FillForegnd.Value = "3";
shape.Fill.FillPattern.Value = 31;

// Add a new star shape
pinX = 2.0;
pinY = 4.5;
long starId = diagram.AddShape(
    pinX, pinY, width, height, starMaster, pageNumber);

// Set the star shape's properties
shape = diagram.Pages[pageNumber].Shapes.GetShape(starId);
shape.Text.Value.Add(new Txt(@"Star text."));
shape.Name = "Star1";
shape.XForm.LocPinX.Ufe.F = "Width*0.5";
shape.XForm.LocPinY.Ufe.F = "Height*0.5";
shape.Line.LineColor.Value = "#ff0000";
shape.Line.LineWeight.Value = 0.03;
shape.Fill.FillBkgnd.Value = "#ff00ff";
shape.Fill.FillForegnd.Value = "#0000ff";
shape.Fill.FillPattern.Value = 31;

// Add a new hexagon shape
pinX = 7.0;
long hexagonId = diagram.AddShape(
    pinX, pinY, width, height, hexagonMaster, pageNumber);

// Set the hexagon shape's properties
shape = diagram.Pages[pageNumber].Shapes.GetShape(hexagonId);
shape.Text.Value.Add(new Txt(@"Hexagon text."));
shape.Name = "Hexagon1";
shape.XForm.LocPinX.Ufe.F = "Width*0.5";
shape.XForm.LocPinY.Ufe.F = "Height*0.5";
shape.Line.LineWeight.Value = 0.03;
shape.Fill.FillPattern.Value = 31;

// Add master to dynamic connector from the stencil
diagram.AddMaster(visioStencil, connectorMaster);

// Connect rectangle and star shapes
Shape connector1 = new Shape();
long connecter1Id = diagram.AddShape(connector1, connectorMaster, 0);
diagram.Pages[0].ConnectShapesViaConnector(rectangleId, ConnectionPointPlace.Bottom,
    starId, ConnectionPointPlace.Top, connecter1Id);

// Connect rectangle and hexagon shapes
Shape connector2 = new Shape();
long connecter2Id = diagram.AddShape(connector2, connectorMaster, 0);
diagram.Pages[0].ConnectShapesViaConnector(rectangleId, ConnectionPointPlace.Bottom,
    hexagonId, ConnectionPointPlace.Left, connecter2Id);

// Save the diagram
diagram.Save(dataDir + "AddConnectShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **استخدم فهارس الاتصال لتوصيل الأشكال**
Aspose.Diagram for .NET API يسمح بالفعل للمطورين بإضافة نقاط اتصال جديدة على الشكل ، ويمكن للمطورين الآن توصيل الأشكال باستخدام فهارس الاتصال.
### **استخدم فهارس الاتصال لتوصيل الأشكال**
يتم عرض عضو ConnectShapesViaConnectorIndex بواسطة ملف[صفحة](https://reference.aspose.com/diagram/net/aspose.diagram/page)يمكن استخدام class لتوصيل الأشكال باستخدام فهارس الاتصال. يوضح الكود التالي كيفية توصيل الأشكال:

1. تهيئة رسم جديد.
1. ضع أربعة أشكال مستطيلة
1. أضف نقطتي اتصال إضافيتين ، بحيث يكون هناك ثلاث نقاط اتصال على خط الحد السفلي
1. قم بتوصيل الشكل الأول من كل اتصال سفلي بأشكال المستطيلات الثلاثة الأخرى من الأعلى باستخدام الموصلات الديناميكية
1. حفظ الرسم
#### **استخدم فهارس الاتصال لتوصيل الأشكال عينة البرمجة**
استخدم الكود التالي في تطبيق .NET الخاص بك لتوصيل الأشكال باستخدام فهارس الاتصال مع Aspose.Diagram for .NET API.

**C#**

{{< highlight "java" >}}

 // initialize a new drawing

Diagram diagram = new Diagram();

// get page by index

Aspose.Diagram.Page page = diagram.Pages[0];

// add masters

string connectorMaster = "Dynamic connector", rectangle = "Rectangle";

int pageNumber = 0;

double width = 2, height = 2, pinX = 4.25, pinY = 9.5;

diagram.AddMaster(@"C:\temp\Basic Shapes.vss", rectangle);

diagram.AddMaster(@"C:\temp\Basic Shapes.vss", connectorMaster);

// add shapes

long shape1_ID = diagram.AddShape(4.5, 7, rectangle, pageNumber);

long shape2_ID = diagram.AddShape(2.25, 4.5, rectangle, pageNumber);

long shape3_ID = diagram.AddShape(4.5, 4.5, rectangle, pageNumber);

long shape4_ID = diagram.AddShape(6.75, 4.5, rectangle, pageNumber);

// get shapes by ID

Aspose.Diagram.Shape shape1 = page.Shapes.GetShape(shape1_ID);

Aspose.Diagram.Shape shape2 = page.Shapes.GetShape(shape2_ID);

Aspose.Diagram.Shape shape3 = page.Shapes.GetShape(shape3_ID);

Aspose.Diagram.Shape shape4 = page.Shapes.GetShape(shape4_ID);

// add two more connection points

Connection connection1 = new Connection();

connection1.X.Ufe.F = "Width*0.33";

connection1.Y.Ufe.F = "Height*0";

Connection connection3 = new Connection();

connection3.X.Ufe.F = "Width*0.66";

connection3.Y.Ufe.F = "Height*0";

shape1.Connections.Add(connection1);

shape1.Connections.Add(connection3);



// add connector shapes

Aspose.Diagram.Shape connector1 = new Aspose.Diagram.Shape();

Aspose.Diagram.Shape connector2 = new Aspose.Diagram.Shape();

Aspose.Diagram.Shape connector3 = new Aspose.Diagram.Shape();

long connecter1Id = diagram.AddShape(connector1, connectorMaster, 0);

long connecter2Id = diagram.AddShape(connector2, connectorMaster, 0);

long connecter3Id = diagram.AddShape(connector3, connectorMaster, 0);

// connect shapes by index of conneecting points

page.ConnectShapesViaConnectorIndex(shape1.ID, 6, shape2.ID, 3, connecter1Id);

page.ConnectShapesViaConnectorIndex(shape1.ID, 1, shape3.ID, 3, connecter2Id);

page.ConnectShapesViaConnectorIndex(shape1.ID, 7, shape4.ID, 3, connecter3Id);

// save drawing

diagram.Save(@"C:\temp\Drawing1_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **استرجع الشكل الأصلي لشكل فرعي**
Aspose.Diagram for .NET يسمح للمطورين باسترجاع الشكل الرئيسي لشكل فرعي.
### **احصل على شكل الوالدين**
ال[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)تقدم الفئة خاصية ParentShape لاسترداد الشكل الأصل.
#### **احصل على نموذج برمجة شكل الوالدين**

{{< highlight csharp >}}
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(13).Shapes.GetShape(2);
Shape parentShape = shape.ParentShape;
Console.WriteLine("Parent Shape's Properties:");
Console.WriteLine("Shape ID: " + parentShape.ID);
Console.WriteLine("Shape Name: " + parentShape.Name);
Console.WriteLine("Shape Type: " + parentShape.Type);
{{< /highlight >}}

