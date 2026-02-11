---
title: تطبيق النسق على الشكل
type: docs
weight: 70
url: /ar/java/apply-theme-to-shape/
description: يشرح هذا القسم كيفية تعيين خصائص النسق في شكل visio باستخدام Aspose.Diagram.
---
## **قم بتعيين لون النسق إلى شكل في Visio**
يوضح هذا الموضوع كيف يمكن للمطورين تطبيق لون النسق على شكل باستخدام Aspose.Diagram for Java.

يوضح الكود أدناه كيفية:

1. تحميل عينة diagram.
1. الحصول على صفحة معينة.
1. الحصول على شكل معين.
1. تعيين موضوع الشكل.
1. احفظ diagram
#### **تعيين السمة إلى نموذج برمجة الشكل**
استخدم الكود التالي في تطبيق Java لتعيين مظهر شكل نوع الموصل باستخدام Aspose.Diagram for Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);
// Load a diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.getPages().getPage("Page-2");

// Add master with stencil file path and master name
String masterName = "Rectangle";
diagram.addMaster(dataDir + "Basic Shapes.vss", masterName);

// Page indexing starts from 0
int PageIndex = 1;
double width = 2, height = 2, pinX = 4.25, pinY = 4.5;
// Add a new rectangle shape
long rectangleId = diagram.addShape(pinX, pinY, width, height, masterName, PageIndex);

// Set shape properties 
Shape rectangle = page.getShapes().getShape(rectangleId);
rectangle.getXForm().getPinX().setValue(5);
rectangle.getXForm().getPinY().setValue(5);
rectangle.setType(TypeValue.SHAPE);
rectangle.getText().getValue().add(new Txt("Aspose Diagram"));

// Apply preset theme clouds to new shape in page "Page-2"
rectangle.setPresetTheme(PresetThemeValue.CLOUDS);
rectangle.setPresetThemeVariant( PresetThemeVariantValue.VARIANT_1);
rectangle.setPresetThemeQuickStyle (PresetQuickStyleValue.VARIANT_STYLE_1);

// Apply preset theme bubble to page "Page-3"
Page page3 = diagram.getPages().getPage("Page-3");
page3.setPresetTheme( PresetThemeValue.BUBBLE);
page3.setPresetThemeVariant(PresetThemeVariantValue.VARIANT_2);
page3.setPresetThemeQuickStyle (PresetQuickStyleValue.VARIANT_STYLE_3);

diagram.save(dataDir + "ApplyThemeToNewShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

