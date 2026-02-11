---
title: العمل مع لصق الأشكال
type: docs
weight: 10
url: /ar/java/working-with-shapes-gluing/
---
## **احصل على الموصلات التي تم لصقها على شكل معين**
[إضافة وتوصيل Visio الأشكال](/diagram/ar/java/add-and-connect-visio-shapes/) يشرح كيفية إضافة شكل وربطه بأشكال أخرى في الرسوم التخطيطية Microsoft Visio باستخدام Aspose.Diagram for Java. من الممكن أيضًا العثور على موصلات ملتصقة بهذا الشكل.
### **الحصول على الأشكال لصقها**
 طريقة GluedShapes المكشوفة بواسطة[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)يمكن استخدام class للحصول على قائمة بمعرفات جميع الموصلات الملصقة بالشكل ، أو إذا كان الشكل المعني موصلًا ، فإن معرفات الأشكال المتصلة به.[ShapeCollection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) يمكن بعد ذلك استخدام class للعثور على شكل من خلال معرفه.

يوضح الكود أدناه كيفية:

1. تحميل ملف عينة.
1. الوصول إلى شكل معين.
1. احصل على قائمة بمعرفات جميع الموصلات الملصقة بهذا الشكل.
#### **الحصول على عينة البرمجة الملصقة للموصلات**
استخدم الكود التالي في تطبيق Java الخاص بك للعثور على جميع الموصلات الملصقة على شكل باستخدام Aspose.Diagram for Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetGluedConnectors.class);   
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "RetrieveShapeInfo.vsd");
// get shape by an ID
Shape shape = diagram.getPages().get(0).getShapes().getShape(90);
// get all glued 1D shapes
long[] gluedShapeIds = shape.gluedShapes(GluedShapesFlags.GLUED_SHAPES_ALL_1_D, null, null);

// display shape ID and name
for (long id : gluedShapeIds)
{
    shape = diagram.getPages().get(0).getShapes().getShape(id);
    System.out.println("ID: " + shape.getID() + "\t\t Name: " + shape.getName());
}

{{< /highlight >}}

## **أشكال الغراء Visio مع نقطة الاتصال**
Aspose.Diagram for Java يتيح للمطورين لصق الأشكال معًا من خلال نقاط الاتصال.
### **أشكال الغراء**
 طريقة GlueShapes المكشوفة بواسطة[صفحة](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) يمكن استخدام الطبقة.

|<p>**المدخلات diagram** </p><p>![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/Z69f4hg.png)</p>|<p>**diagram بعد لصق الأشكال** </p><p>![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/5TJpDwc.png)</p>|
|:- |:- |
يوضح الكود أدناه كيفية:

1. تحميل ملف عينة.
1. أشكال الغراء.
1. وفر diagram.
#### **عينة لبرمجة الأشكال الغراء Visio**
استخدم الكود التالي في تطبيق Java للصق الأشكال عبر نقاط الاتصال:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GlueVisioShapes.class);
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.getPages().getPage("Page-1");
// set shape id
long shape1_ID = 7;
long shape2_ID = 494;
// Glue shapes
page.glueShapes(shape1_ID, ConnectionPointPlace.CENTER, shape2_ID);

// Save diagram
diagram.save(dataDir + "GlueVisioShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **أشكال الغراء داخل الحاوية**
Aspose.Diagram for Java يتيح للمطورين لصق أشكال المجموعة داخل الحاوية.
### **شكل مجموعة الغراء**
يمكن استخدام أسلوب GlueShapesInContainer المكشوف بواسطة فئة الصفحة.

|<p>**المدخلات diagram** </p><p>![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/HRRzIEh.png)</p>|<p>**diagram بعد لصق أشكال المجموعة** </p><p>![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/YxCiOgU.png)</p>|
|:- |:- |
يوضح الكود أدناه كيفية:

1. تحميل ملف عينة.
1. أشكال مجموعة الغراء.
1. وفر diagram.
#### **أشكال الغراء داخل عينة البرمجة**
استخدم الكود التالي في تطبيق Java للصق شكل المجموعة داخل الحاوية:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GlueContainerShape.class);   
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.getPages().getPage("Page-1");

// The ID of shape which is glue from Aspose.Diagram.Shape.
long shapeFromId = 779;
// The location on the first connection index where to glue
int shapeToBeginConnectionIndex = 72;
// The location on the end connection index where to glue
int shapeToEndConnectionIndex = 73;
// The ID of shape where to glue to Aspose.Diagram.Shape.
long shapeToId = 743;

// Glue shapes in container
page.glueShapesInContainer(shapeFromId, shapeToBeginConnectionIndex, shapeToEndConnectionIndex, shapeToId);

// Glue shapes in container using connection name
// page.GlueShapesInContainer(fasId, "U05L", "U05R", cabinetId1);

// Save diagram
diagram.save(dataDir + "GlueContainerShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

