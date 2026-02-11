---
title: تدوير وتغيير الموضع وتوصيل الأشكال الفرعية
type: docs
weight: 60
url: /ar/java/rotate-change-the-position-and-connect-sub-shapes/
---
## **قم بتدوير شكل بزاوية مناسبة**
 Aspose.Diagram for Java يسمح لك بتدوير شكل إلى أي زاوية. تعرض طريقة SetAngle بواسطة ملف[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) يمكن استخدام class لتدوير الشكل إلى أي زاوية مرغوبة. يأخذ معلمة واحدة كزاوية.
### **قم بتدوير عينة برمجة الشكل**
استخدم الكود التالي في تطبيق Java لتدوير شكل باستخدام Aspose.Diagram for Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RotateVisioShape.class); 
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");
// get shape by id
Shape shape = page.getShapes().getShape(16);

// Add a shape and set the angle
shape.setAngle(190);

// Save diagram
diagram.save(dataDir + "RotateVisioShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **تغيير موضع الشكل**
تسمح لك فئة الشكل بتغيير موضع الشكل. يتم ضبط خط الموصل تلقائيًا عند نقل الشكل إلى موضع مختلف.

تدعم طريقتا Move و MoveTo ، اللتان تعرضهما فئة الشكل ، تغيير موضع الشكل كجزء من مجموعة أم لا.
تعمل أمثلة التعليمات البرمجية في هذه المقالة على نقل شكل على الصفحة.
**المدخلات diagram** 

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/cThgWnB.png)


**diagram بعد نقل الشكل** 

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/Q3QByqe.png)

عملية تحريك الشكل هي:

1. قم بتحميل diagram.
1. ابحث عن شكل معين.
1. انقل الشكل إلى موقع مختلف
1. احفظ diagram.
### **نموذج برمجة تغيير الموضع**
يوضح مقتطف الشفرة أدناه كيفية تحريك الشكل. يسترجع الكود صفحة Visio بالاسم والشكل بواسطة المعرف 16 ، وينقل موضعه.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(MoveVisioShape.class);  
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");
// get shape by id
Shape shape = page.getShapes().getShape(16);
// move shape from its position, it adds values in coordinates
shape.move(1, 1);

// save diagram
diagram.save(dataDir + "MoveVisioShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **ربط الأشكال الفرعية للمجموعات**
يوضح هذا الموضوع كيفية توصيل شكلين فرعيين من شكلين مختلفين للمجموعة في مخطط Microsoft Visio باستخدام Aspose.Diagram for Java.

 تعرض طريقة ConnectShapesViaConnector بواسطة ملف[صفحة](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) يمكن استخدام class لتوصيل الأشكال بمعرفاتها. طريقة AddShape ، المكشوفة بواسطة ملف[Diagram](https://reference.aspose.com/diagram/java)فئة ، يمكن استخدامها لإضافة شكل.

|<p>**المدخلات diagram** </p><p>![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/74rDby5.png)</p>|<p>**diagram بعد توصيل الأشكال الفرعية** </p><p>![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/c387dZJ.png)</p>|
|:- |:- |
يوضح الكود أدناه كيفية:

1. تحميل ملف عينة.
1. الوصول إلى صفحة معينة.
1. أضف شكل الموصل الديناميكي إلى الصفحة المحددة.
1. ربط الأشكال الفرعية
### **عينة برمجة توصيل الأشكال الفرعية**
استخدم الكود التالي في تطبيق Java الخاص بك لتوصيل الأشكال الفرعية لاثنين من أشكال المجموعة المختلفة باستخدام Aspose.Diagram for Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ConnectVisioSubShapes.class);   
// set sub shape ids
long shapeFromId = 2;
long shapeToId = 4;

// load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// access a particular page
Page page = diagram.getPages().getPage("Page-3");
       
// initialize connector shape
Shape shape = new Shape();
shape.getLine().getEndArrow().setValue(4);
shape.getLine().getLineWeight().setValue(0.01388);

// add shape
long connecter1Id = diagram.addShape(shape, "Dynamic connector", page.getID());
// connect sub-shapes
page.connectShapesViaConnector(shapeFromId, ConnectionPointPlace.RIGHT, shapeToId, ConnectionPointPlace.LEFT, connecter1Id);
// save Visio drawing
diagram.save(dataDir + "ConnectVisioSubShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **اجعل الأشكال متصلة بشكل معين**
[إضافة وتوصيل Visio الأشكال](/diagram/ar/java/add-and-connect-visio-shapes/) يشرح كيفية إضافة شكل وربطه بأشكال أخرى في الرسوم التخطيطية Microsoft Visio باستخدام Aspose.Diagram for Java. من الممكن أيضًا العثور على أشكال متصلة بشكل معين.

 تعرض طريقة ConnectedShapes بواسطة ملف[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) يمكن استخدام class للحصول على معرفات الأشكال المتصلة بالشكل. طريقة GetShape ، المكشوفة بواسطة ملف[ShapeCollection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) يمكن بعد ذلك استخدام class للعثور على شكل من خلال معرفه.

يوضح الكود أدناه كيفية:

1. تحميل ملف عينة.
1. الوصول إلى شكل معين.
1. احصل على أسماء جميع الأشكال المتصلة بالشكل المحدد.
### **احصل على عينة برمجة الأشكال**
استخدم الكود التالي في تطبيق Java الخاص بك للعثور على جميع الأشكال المتصلة بشكل معين باستخدام Aspose.Diagram for Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetAllConnectedShapes.class);
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get shape by id
Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(16);
// get connected shapes
long[] connectedShapeIds = shape.connectedShapes(ConnectedShapesFlags.CONNECTED_SHAPES_ALL_NODES, null);

for (long id : connectedShapeIds)
{
    shape = diagram.getPages().getPage("Page-3").getShapes().getShape(id);
    System.out.println("ID: " + shape.getID() + "\t\t Name: " + shape.getName());
}

{{< /highlight >}}

