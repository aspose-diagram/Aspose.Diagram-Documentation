---
title: تحويل Visio شكل إلى صورة
type: docs
weight: 10
url: /ar/net/convert-a-visio-shape-to-image/
description: يشرح هذا القسم كيفية تحويل شكل visio إلى صورة باستخدام Aspose.Diagram.
---
## **تحويل شكل visio إلى صورة**
يوضح هذا الموضوع كيف يمكن للمطورين تحويل شكل visio إلى صورة باستخدام Aspose.Diagram.
 طريقة ToImage التي كشفها ملف[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) يمكن استخدام فئة للتحويل إلى صورة.


يوضح الكود أدناه كيفية:

1. تحميل عينة diagram.
1. الحصول على صفحة معينة.
1. الحصول على شكل معين.
1. تحويل الشكل إلى صورة.
#### **عينة برمجة من شكل إلى صورة**
استخدم الكود التالي في تطبيق .net لتحويل شكل visio إلى صورة.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToImage.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

// Shape to Image
Aspose.Diagram.Saving.ImageSaveOptions o = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);
shape.ToImage("out.png", o);

{{< /highlight >}}

