---
title: أضف نقطة الاتصال إلى الشكل
type: docs
weight: 70
url: /ar/net/add-connection-point-to-shape/
description: يشرح هذا القسم كيفية إضافة نقطة اتصال إلى شكل visio مع Aspose.Diagram.
---
## **أضف نقطة اتصال إلى شكل في Visio**
يوضح هذا الموضوع كيف يمكن للمطورين إضافة نقطة اتصال إلى شكل visio باستخدام Aspose.Diagram for .NET.
### **أضف نقطة اتصال**
 ال[روابط](https://reference.aspose.com/diagram/net/aspose.diagram/shape/properties/connections) يمثل الكائن مجموعة الاتصال في[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) صف دراسي.

يوضح الكود أدناه كيفية:

1. تحميل عينة diagram.
1. الحصول على صفحة معينة.
1. الحصول على شكل معين.
1. اتصال جديد
1.  تعيين خاصية الاتصال
1. إضافة اتصال بالشكل
1. احفظ diagram
#### **أضف نقطة اتصال لتشكيل نموذج البرمجة**
استخدم الكود التالي في تطبيق .NET لإضافة اتصال إلى شكل باستخدام Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");

// Get a particular page
Page page = diagram.Pages.GetPage("Page-3");
// Get a dynamic connector type shape by id
Shape shape = page.Shapes.GetShape(18);
// Set dynamic connector appearance
shape.SetConnectorsType(ConnectorsTypeValue.StraightLines);

// Saving Visio diagram
diagram.Save(dataDir + "SetConnectorAppearance_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

