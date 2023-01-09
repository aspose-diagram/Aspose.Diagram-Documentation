---
title: استخدم فهارس الاتصال لتوصيل الأشكال
type: docs
weight: 20
url: /ar/java/use-connection-indexes-to-connect-shapes/
---
## **أضف اتصالات جديدة على الشكل واستخدم فهارس الاتصال لتوصيل الأشكال**
Aspose.Diagram for Java API يساعد المطورين على إضافة نقاط اتصال جديدة على الشكل ، ويمكن للمطورين الآن توصيل الأشكال بفهارس الاتصال.
### **استخدم فهارس الاتصال لتوصيل الأشكال**
تم الكشف عن عضو connectShapesViaConnectorIndex بواسطة ملف[صفحة](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page)يمكن استخدام class لتوصيل الأشكال باستخدام فهارس الاتصال. يوضح الكود التالي كيفية توصيل الأشكال:

1. تهيئة رسم جديد.
1. ضع أربعة أشكال مستطيلة
1. أضف نقطتي اتصال إضافيتين ، بحيث يكون هناك ثلاث نقاط اتصال على خط الحد السفلي
1. قم بتوصيل الشكل الأول من كل اتصال سفلي بأشكال المستطيلات الثلاثة الأخرى من الأعلى باستخدام الموصلات الديناميكية
1. حفظ الرسم
#### **استخدام فهارس الاتصال لتوصيل الأشكال عينة البرمجة**
استخدم الكود التالي في تطبيق Java الخاص بك لتوصيل الأشكال بفهارس الاتصال بـ Aspose.Diagram for Java API.

**Java**

{{< highlight "java" >}}

 // initialize a new drawing

Diagram diagram = new Diagram();

// get page by index

Page page = diagram.getPages().get(0);

// add masters

String connectorMaster = "Dynamic connector", rectangle = "Rectangle";

int pageNumber = 0;

double width = 2, height = 2, pinX = 4.25, pinY = 9.5;

diagram.addMaster("C:\\temp\\Basic Shapes.vss", rectangle);

diagram.addMaster("C:\\temp\\Basic Shapes.vss", connectorMaster);

// add shapes

long shape1_ID = diagram.addShape(4.5, 7, rectangle, pageNumber);

long shape2_ID = diagram.addShape(2.25, 4.5, rectangle, pageNumber);

long shape3_ID = diagram.addShape(4.5, 4.5, rectangle, pageNumber);

long shape4_ID = diagram.addShape(6.75, 4.5, rectangle, pageNumber);

// get shapes by ID

Shape shape1 = page.getShapes().getShape(shape1_ID);

Shape shape2 = page.getShapes().getShape(shape2_ID);

Shape shape3 = page.getShapes().getShape(shape3_ID);

Shape shape4 = page.getShapes().getShape(shape4_ID);

// add two more connection points

Connection connection1 = new Connection();

connection1.getX().getUfe().setF("Width*0.33");

connection1.getY().getUfe().setF("Height*0");

Connection connection3 = new Connection();

connection3.getX().getUfe().setF("Width*0.66");

connection3.getY().getUfe().setF("Height*0");

connection1.setIX(shape1.getConnections().add(connection1));

connection3.setIX( shape1.getConnections().add(connection3));

// add connector shapes

Shape connector1 = new Shape();

Shape connector2 = new Shape();

Shape connector3 = new Shape();

long connecter1Id = diagram.addShape(connector1, connectorMaster, 0);

long connecter2Id = diagram.addShape(connector2, connectorMaster, 0);

long connecter3Id = diagram.addShape(connector3, connectorMaster, 0);

// connect shapes by index of conneecting points
page.connectShapesViaConnectorIndex(shape1.getID(), 6, shape2.getID(), 3, connecter1Id);
page.connectShapesViaConnectorIndex(shape1.getID(), 1, shape3.getID(), 3, connecter2Id);


// save drawing

diagram.save("C:\\temp\\Drawing1_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
