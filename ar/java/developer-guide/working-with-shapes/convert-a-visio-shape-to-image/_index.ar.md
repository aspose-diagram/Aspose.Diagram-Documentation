---
title: تحويل Visio شكل إلى صورة
type: docs
weight: 10
url: /ar/java/convert-a-visio-shape-to-image/
description: يشرح هذا القسم كيفية تحويل شكل visio إلى صورة باستخدام Aspose.Diagram.
---
## **تحويل شكل visio إلى صورة**
 طريقة ToImage التي كشفها ملف[شكل](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) يمكن استخدام فئة للتحويل إلى صورة.

يوضح الكود أدناه كيفية:

1. تحميل عينة diagram.
1. الحصول على صفحة معينة.
1. الحصول على شكل معين.
1. تحويل الشكل إلى صورة.
### **شكل على صورة**
استخدم الكود التالي في تطبيق java لتحويل شكل visio إلى صورة.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ShapeToImage.class); 
// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToImage.vsdx");

// Get a particular page
Page page = diagram.getPages().get(0);

// Get a particular shape
Shape shape = page.getShapes().get(0);

// Shape to image
com.aspose.diagram.ImageSaveOptions option = new com.aspose.diagram.ImageSaveOptions(SaveFileFormat.PNG);
shape.toImage("out.png",option);
{{< /highlight >}}
```


