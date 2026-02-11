---
title: احصل على Visio Shape Inherit Fill
type: docs
weight: 100
url: /ar/java/get-visio-shape-inherit-fill/
description: يشرح هذا القسم كيفية الحصول على نمط تعبئة الشكل visio الموروث من النمط الأصل والشكل الرئيسي باستخدام Aspose.Diagram.
---
### **استرجع بيانات التعبئة الموروثة لشكل Visio**
يمكن أن ترث أشكال Visio النمط الأصل والشكل الرئيسي. قد يحصل المطورون على بيانات التعبئة الموروثة لشكل Visio. الخاصية InheritFill ، المكشوفة بواسطة[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class ، تحتوي على قيم تنسيق التعبئة للشكل الذي يرثه النمط الأصل والشكل الرئيسي.
#### **استرجاع نموذج برمجة بيانات التعبئة الموروثة**
يسترد مقتطف التعليمات البرمجية التالي بيانات التعبئة الموروثة للشكل. يرجى التحقق من نموذج الكود هذا:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveInheritedFillData.class) + "Shapes/";

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.getPages().getPage("Page-1");
// Get shape by ID
Shape shape = page.getShapes().getShape(1);
// Get the fill formatting values
System.out.println(shape.getInheritFill().getFillBkgnd().getValue());
System.out.println(shape.getInheritFill().getFillForegnd().getValue());
System.out.println(shape.getInheritFill().getFillPattern().getValue());
System.out.println(shape.getInheritFill().getShapeShdwObliqueAngle().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetX().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetY().getValue());
System.out.println(shape.getInheritFill().getShapeShdwScaleFactor().getValue());
System.out.println(shape.getInheritFill().getShapeShdwType().getValue());
System.out.println(shape.getInheritFill().getShdwBkgnd().getValue());
System.out.println(shape.getInheritFill().getShdwBkgndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwForegnd().getValue());
System.out.println(shape.getInheritFill().getShdwForegndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwPattern().getValue());

{{< /highlight >}}


