---
title: تدوير وتغيير الموضع وتوصيل الأشكال الفرعية
type: docs
weight: 30
url: /ar/net/rotate-change-the-position-and-connect-sub-shapes/
description: يشرح هذا القسم كيفية تدوير شكل visio باستخدام Aspose.Diagram.
---
## **قم بتدوير شكل بزاوية مناسبة**
 Aspose.Diagram for .NET يسمح لك بتدوير شكل إلى أي زاوية. تعرض طريقة SetAngle بواسطة ملف[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) يمكن استخدام class لتدوير الشكل إلى أي زاوية مرغوبة. يأخذ معلمة واحدة كزاوية.
### **قم بتدوير عينة برمجة الشكل**
استخدم الكود التالي في تطبيق .NET لتدوير شكل باستخدام Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");
// Get shape by id
Shape shape = page.Shapes.GetShape(16);

// Add a shape and set the angle
shape.SetAngle(190);

// Save diagram
diagram.Save(dataDir + "RotateVisioShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **تغيير موضع الشكل**
 ال[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) تسمح لك الفئة بتغيير موضع الشكل. يتم ضبط خط الموصل تلقائيًا عند نقل الشكل إلى موضع مختلف. أساليب Move و MoveTo ، المكشوفة بواسطة[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) فئة ، دعم تغيير موضع الشكل كجزء من مجموعة أم لا. تعمل أمثلة التعليمات البرمجية في هذه المقالة على نقل شكل على الصفحة.

عملية تحريك الشكل هي:

1. قم بتحميل diagram.
1. ابحث عن شكل معين.
1. انقل الشكل إلى موقع مختلف
1. احفظ diagram.
### **نموذج برمجة تغيير الموضع**
يوضح مقتطف الشفرة أدناه كيفية تحريك الشكل. يسترجع الكود صفحة Visio بالاسم والشكل بواسطة المعرف 16 ، وينقل موضعه.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");
// Get shape by id
Shape shape = page.Shapes.GetShape(16);
// Move shape from its position, it adds values in coordinates
shape.Move(1, 1);

// Save diagram
diagram.Save(dataDir + "MoveVisioShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **ربط الأشكال الفرعية للمجموعات**
 يوضح هذا الموضوع كيفية توصيل شكلين فرعيين من شكلين مختلفين للمجموعة في مخطط Microsoft Visio باستخدام Aspose.Diagram for .NET.[صفحة](http://www.aspose.com/api/net/diagram/aspose.diagram/page) يمكن استخدام class لتوصيل الأشكال بمعرفاتها. طريقة AddShape ، المكشوفة بواسطة ملف[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)فئة ، يمكن استخدامها لإضافة شكل.

يوضح الكود أدناه كيفية:

1. تحميل ملف عينة.
1. الوصول إلى صفحة معينة.
1. أضف شكل الموصل الديناميكي إلى الصفحة المحددة.
1. ربط الأشكال الفرعية
### **عينة برمجة توصيل الأشكال الفرعية**
استخدم الكود التالي في تطبيق .NET الخاص بك لتوصيل الأشكال الفرعية لاثنين من أشكال المجموعة المختلفة باستخدام Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Set sub shape ids
long shapeFromId = 2;
long shapeToId = 4;

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Access a particular page
Page page = diagram.Pages.GetPage("Page-3");
           
// Initialize connector shape
Shape shape = new Shape();
shape.Line.EndArrow.Value = 4;
shape.Line.LineWeight.Value = 0.01388;

// Add shape
long connecter1Id = diagram.AddShape(shape, "Dynamic connector", page.ID);
// Connect sub-shapes
page.ConnectShapesViaConnector(shapeFromId, ConnectionPointPlace.Right, shapeToId, ConnectionPointPlace.Left, connecter1Id);
// Save Visio drawing
diagram.Save(dataDir + "ConnectVisioSubShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **اجعل الأشكال متصلة بشكل معين**
[إضافة وتوصيل Visio الأشكال](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) يشرح كيفية إضافة شكل وربطه بأشكال أخرى في الرسوم التخطيطية Microsoft Visio باستخدام Aspose.Diagram for .NET. من الممكن أيضًا العثور على أشكال متصلة بشكل معين.

 تعرض طريقة ConnectedShapes بواسطة ملف[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) يمكن استخدام class للحصول على معرفات الأشكال المتصلة بالشكل. طريقة GetShape ، المكشوفة بواسطة ملف[ShapeCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) يمكن بعد ذلك استخدام class للعثور على شكل من خلال معرفه.

يوضح الكود أدناه كيفية:

1. تحميل ملف عينة.
1. الوصول إلى شكل معين.
1. احصل على أسماء جميع الأشكال المتصلة بالشكل المحدد.
### **احصل على عينة برمجة الأشكال**
استخدم الكود التالي في تطبيق .NET الخاص بك للعثور على جميع الأشكال المتصلة بشكل معين باستخدام Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get shape by id
Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(16);
// Get connected shapes
long[] connectedShapeIds = shape.ConnectedShapes(ConnectedShapesFlags.ConnectedShapesAllNodes, null);

foreach (long id in connectedShapeIds)
{
    shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(id);
    Console.WriteLine("ID: " + shape.ID + "\t\t Name: " + shape.Name);
}

{{< /highlight >}}

