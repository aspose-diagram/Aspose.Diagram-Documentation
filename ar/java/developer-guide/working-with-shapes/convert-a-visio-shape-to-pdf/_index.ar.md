---
title: تحويل شكل Visio إلى PDF
type: docs
weight: 10
url: /ar/java/convert-a-visio-shape-to-pdf/
description: يشرح هذا القسم كيفية تحويل شكل visio إلى pdf باستخدام Aspose.Diagram.
---
## ** تحويل شكل visio إلى pdf**
 طريقة ToPdf التي كشفها ملف[شكل](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) يمكن استخدام class للتحويل إلى pdf.

يوضح الكود أدناه كيفية:

1. تحميل عينة diagram.
1. الحصول على صفحة معينة.
1. الحصول على شكل معين.
1. تحويل الشكل إلى pdf.
### **شكل لقوات الدفاع الشعبي**
استخدم الكود التالي في تطبيق java لتحويل شكل visio إلى pdf.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ShapeToPdf.class); 
// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToPdf.vsdx");

// Get a particular page
Page page = diagram.getPages().get(0);

// Get a particular shape
Shape shape = page.getShapes().get(0);

// Shape to Pdf
shape.toPdf("out.pdf");
{{< /highlight >}}



