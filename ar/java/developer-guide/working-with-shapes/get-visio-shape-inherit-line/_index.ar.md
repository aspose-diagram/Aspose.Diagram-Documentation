---
title: احصل على Visio Shape Inherit Line
type: docs
weight: 100
url: /ar/java/get-visio-shape-inherit-line/
description: يشرح هذا القسم كيفية الحصول على نمط خط الشكل visio الموروث من النمط الأصلي والشكل الرئيسي باستخدام Aspose.Diagram.
---
### **استرجع بيانات الخط الموروث لشكل Visio**
 يمكن أن ترث أشكال Visio النمط الأصل والشكل الرئيسي. يمكن للمطورين الحصول على بيانات خط التوريث لشكل Visio أو تعيينها. الخاصية InheritLine ، المكشوفة بواسطة[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class ، تحتوي على قيم تنسيق الخط للشكل الذي يرثه النمط الأصل والشكل الرئيسي.
#### **استرجاع نموذج برمجة بيانات الخط الموروث**
يسترد مقتطف التعليمات البرمجية التالي بيانات الخط الموروثة للشكل. يرجى التحقق من نموذج الكود هذا:

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveInheritedLine.class) + "Shapes/";

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.getPages().getPage("Page-1");
// Get shape by ID
Shape shape = page.getShapes().getShape(1);
//Get Inherit Line from the parent style and master
Line line = shape.getInheritLine();
// Get the line formatting values
System.out.println(line.getBeginArrow().getValue());
System.out.println(line.getBeginArrowSize().getValue());
System.out.println(line.getEndArrow().getValue());
System.out.println(line.getEndArrowSize().getValue());
System.out.println(line.getLineColor().getValue());
System.out.println(line.getLinePattern().getValue());
System.out.println(line.getLineWeight().getValue());
System.out.println(line.getRounding().getValue());

{{< /highlight >}}
```

