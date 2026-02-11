---
title: ربط الأشكال
type: docs
weight: 90
url: /ar/net/connect-shapes/
description: يشرح هذا القسم كيفية توصيل شكلين بـ Aspose.Diagram.
---
## **ربط الأشكال**
يوضح هذا القسم كيفية توصيل شكلين باستخدام Aspose.Diagram for .NET.
### **ربط الأشكال**
 ال[ConnectShapesViaConnector](https://reference.aspose.com/diagram/net/aspose.diagram.page/connectshapesviaconnector/methods/1) طريقة توصيل شكلين via موصل في[صفحة](http://www.aspose.com/api/net/diagram/aspose.diagram/page) صف دراسي.

يوضح الكود أدناه كيفية:

1. قم بإنشاء diagram من الاستنسل.
1. أضف شكلين مستطيلين إلى الصفحة.
1. أضف شكل موصل إلى الصفحة.
1. قم بتوصيل المستطيلين بالموصل باستخدام ConnectShapesViaConnector mothod
1. احفظ diagram
#### **عينة برمجة ربط الأشكال**
استخدم الكود التالي في تطبيق .NET الخاص بك لتوصيل الأشكال باستخدام Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
string stencil = dataDir + "Basic Shapes.vss";

// create a diagram from stencil
Diagram diagram = new Diagram(stencil);
string connectorMaster = "Dynamic connector";
string rectangleMaster = "Rectangle";
// add two rectangles to page 0
long rectangle1 = diagram.AddShape(2, 2, rectangleMaster, 0);
long rectangle2 = diagram.AddShape(2, 4, rectangleMaster, 0);
// add a connector to page 0
Shape connector1 = new Shape();
long connecter1Id = diagram.AddShape(connector1, connectorMaster, 0);
// connect the two rectangles with the connector
diagram.Pages[0].ConnectShapesViaConnector(rectangle1, ConnectionPointPlace.Right, rectangle2, ConnectionPointPlace.Bottom, connecter1Id);

// If the connection of shapes has name, we also could use connection name to connect like below
//diagram.Pages[0].ConnectShapesViaConnector(shape1, "Port7", shape2, "Port21", connecter1Id);
// The code line above is equal to the below two lines
//diagram.Pages[0].GlueShapeToConnectorBeginX(shape1, "Port7", connecter1Id);
//diagram.Pages[0].GlueShapeToConnectorEndX(shape2, "Port21", connecter1Id);

// Save diagram
diagram.Save(dataDir + "ConnectShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


|**نتيجة**|
|:- |
|![ConnectShapes_out.vsdx](ConnectShapes.png)|
