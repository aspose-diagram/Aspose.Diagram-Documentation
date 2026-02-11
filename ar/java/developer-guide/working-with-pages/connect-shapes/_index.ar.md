---
title: ربط الأشكال
type: docs
weight: 90
url: /ar/java/connect-shapes/
description: يشرح هذا القسم كيفية توصيل شكلين بـ Aspose.Diagram for Java.
---
## **ربط الأشكال**
يوضح هذا القسم كيفية توصيل شكلين باستخدام Aspose.Diagram for Java.
### **ربط الأشكال**
 ال[connectShapesViaConnector](https://reference.aspose.com/diagram/java/com.aspose.diagram/page#connectShapesViaConnector(long,%20int,%20long,%20int,%20long) ) طريقة توصيل شكلين via موصل في[صفحة](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) صف دراسي.

يوضح الكود أدناه كيفية:

1. قم بإنشاء diagram من الاستنسل.
1. أضف شكلين مستطيلين إلى الصفحة.
1. أضف شكل موصل إلى الصفحة.
1. قم بتوصيل المستطيلين بالموصل باستخدام connectShapesViaConnector mothod
1. احفظ diagram
#### **عينة برمجة ربط الأشكال**
استخدم الكود التالي لتوصيل الأشكال باستخدام Aspose.Diagram for Java.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ConnectShapes.class);
String stencil = dataDir + "Basic Shapes.vss";

// create a diagram from stencil
Diagram diagram = new Diagram(stencil);
String connectorMaster = "Dynamic connector";
String rectangleMaster = "Rectangle";
// add two rectangles to page 0
long rectangle1 = diagram.addShape(2, 2, rectangleMaster, 0);
long rectangle2 = diagram.addShape(2, 4, rectangleMaster, 0);
// add a connector to page 0
Shape connector1 = new Shape();
long connecter1Id = diagram.addShape(connector1, connectorMaster, 0);
// connect the two rectangles with the connector
diagram.getPages().get(0).connectShapesViaConnector(rectangle1, ConnectionPointPlace.RIGHT, rectangle2, ConnectionPointPlace.BOTTOM, connecter1Id);

// If the connection of shapes has name, we also could use connection name to connect like below
//diagram.getPages().get(0).connectShapesViaConnector(shape1, "Port7", shape2, "Port21", connecter1Id);
// The code line above is equal to the below two lines
//diagram.getPages().get(0).glueShapeToConnectorBeginX(shape1, "Port7", connecter1Id);
//diagram.getPages().get(0).glueShapeToConnectorEndX(shape2, "Port21", connecter1Id);

// Save diagram
diagram.save(dataDir + "ConnectShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

|**نتيجة**|
|:- |
|![ConnectShapes_out.vsdx](ConnectShapes.png)|
