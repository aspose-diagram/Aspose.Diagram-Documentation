---
title: تحويل شكل Visio إلى Svg
type: docs
weight: 10
url: /ar/java/convert-a-visio-shape-to-svg/
description: يشرح هذا القسم كيفية تحويل شكل visio إلى svg باستخدام Aspose.Diagram.
---
## ** تحويل شكل visio إلى svg**
 طريقة ToSvg المكشوفة بواسطة ملف[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) يمكن استخدام class للتحويل إلى svg.

يوضح الكود أدناه كيفية:

1. تحميل عينة diagram.
1. الحصول على صفحة معينة.
1. الحصول على شكل معين.
1. تحويل الشكل إلى svg.
### **شكل إلى Svg**
استخدم الكود التالي في تطبيق java لتحويل شكل visio إلى svg.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ShapeToSvg.class); 
// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToSvg.vsdx");

// Get a particular page
Page page = diagram.getPages().get(0);

// Get a particular shape
Shape shape = page.getShapes().get(0);

// Shape to Svg
SVGSaveOptions option = new SVGSaveOptions();
shape.toSvg("out.svg",option);
{{< /highlight >}}



