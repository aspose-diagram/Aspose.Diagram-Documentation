---
title: العمل مع لصق الأشكال
type: docs
weight: 40
url: /ar/net/working-with-shapes-gluing/
description: يشرح هذا القسم كيفية الحصول على الأشكال التي يتم لصقها بشكل معين باستخدام Aspose.Diagram.
---
## **احصل على الموصلات التي تم لصقها على شكل معين**
[إضافة وتوصيل Visio الأشكال](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) يشرح كيفية إضافة شكل وربطه بأشكال أخرى في الرسوم التخطيطية Microsoft Visio باستخدام Aspose.Diagram for .NET. من الممكن أيضًا العثور على موصلات ملتصقة بهذا الشكل.
### **الحصول على الأشكال لصقها**
 طريقة GluedShapes المكشوفة بواسطة[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)يمكن استخدام class للحصول على قائمة بمعرفات جميع الموصلات الملصقة بالشكل ، أو إذا كان الشكل المعني موصلًا ، فإن معرفات الأشكال المتصلة به.[ShapeCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) يمكن بعد ذلك استخدام class للعثور على شكل من خلال معرفه.

يوضح الكود أدناه كيفية:

1. تحميل ملف عينة.
1. الوصول إلى شكل معين.
1. احصل على قائمة بمعرفات جميع الموصلات الملصقة بهذا الشكل.
#### **الحصول على عينة البرمجة الملصقة للموصلات**
استخدم الكود التالي في تطبيق .NET الخاص بك للعثور على جميع الموصلات الملصقة على شكل باستخدام Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "RetrieveShapeInfo.vsd");
// Get shape by an ID
Shape shape = diagram.Pages[0].Shapes.GetShape(90);
// Get all glued 1D shapes
long[] gluedShapeIds = shape.GluedShapes(GluedShapesFlags.GluedShapesAll1D, null, null);

// Display shape ID and name
foreach (long id in gluedShapeIds)
{
    shape = diagram.Pages[0].Shapes.GetShape(id);
    Console.WriteLine("ID: " + shape.ID + "\t\t Name: " + shape.Name);
}

{{< /highlight >}}

## **أشكال الغراء Visio مع نقطة الاتصال**
Aspose.Diagram for .NET يتيح للمطورين لصق الأشكال معًا من خلال نقاط الاتصال.
### **أشكال الغراء**
 طريقة GlueShapes المكشوفة بواسطة[صفحة](http://www.aspose.com/api/net/diagram/aspose.diagram/page) يمكن استخدام الطبقة.

|<p>**المدخلات diagram** </p><p>![ما يجب القيام به: image_بديل_نص](working-with-shapes-gluing_1.png)</p>|<p>**diagram بعد لصق الأشكال** </p><p>![ما يجب القيام به: image_بديل_نص](working-with-shapes-gluing_2.png)</p>|
|:- |:- |
يوضح الكود أدناه كيفية:

1. تحميل ملف عينة.
1. أشكال الغراء.
1. وفر diagram.
#### **عينة لبرمجة الأشكال الغراء Visio**
استخدم الكود التالي في تطبيق .NET للصق الأشكال عبر نقاط الاتصال:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.Pages.GetPage("Page-1");
// Set shape id
long shape1_ID = 7;
long shape2_ID = 494;
// Glue shapes
page.GlueShapes(shape1_ID, Aspose.Diagram.Manipulation.ConnectionPointPlace.Center, shape2_ID);

// Save diagram
diagram.Save(dataDir + "GlueVisioShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **أشكال الغراء داخل الحاوية**
Aspose.Diagram for .NET يتيح للمطورين لصق أشكال المجموعة داخل الحاوية.
### **شكل مجموعة الغراء**
 تم الكشف عن أسلوب GlueShapesInContainer بواسطة ملف[صفحة](http://www.aspose.com/api/net/diagram/aspose.diagram/page) يمكن استخدام الطبقة.

|<p>**المدخلات diagram** </p><p>![ما يجب القيام به: image_بديل_نص](working-with-shapes-gluing_3.png)</p>|<p>**diagram بعد لصق أشكال المجموعة** </p><p>![ما يجب القيام به: image_بديل_نص](working-with-shapes-gluing_4.png)</p>|
|:- |:- |
يوضح الكود أدناه كيفية:

1. تحميل ملف عينة.
1. أشكال مجموعة الغراء.
1. وفر diagram.
#### **أشكال الغراء داخل عينة البرمجة**
استخدم الكود التالي في تطبيق .NET للصق شكل المجموعة داخل الحاوية:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.Pages.GetPage("Page-1");

// The ID of shape which is glue from Aspose.Diagram.Shape.
long shapeFromId = 779;
// The location on the first connection index where to glue
int shapeToBeginConnectionIndex = 72;
// The location on the end connection index where to glue
int shapeToEndConnectionIndex = 73;
// The ID of shape where to glue to Aspose.Diagram.Shape.
long shapeToId = 743;

// Glue shapes in container
page.GlueShapesInContainer(shapeFromId, shapeToBeginConnectionIndex, shapeToEndConnectionIndex, shapeToId);

// Glue shapes in container using connection name
// Page.GlueShapesInContainer(fasId, "U05L", "U05R", cabinetId1);

// Save diagram
diagram.Save(dataDir + "GlueContainerShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

