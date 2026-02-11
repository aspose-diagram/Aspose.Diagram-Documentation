---
title: العمل مع مربعات النص
type: docs
weight: 200
url: /ar/java/working-with-text-boxes/
---
## **تنسيق النص في مقطع كتلة نص الشكل Visio**
 Aspose.Diagram API يسمح للمطورين بالتحكم في اتجاه النص والمحاذاة والهوامش ولون الخلفية وشفافية لون الخلفية وموضع إيقاف علامة الجدولة الافتراضي للنص في كتلة نص الشكل. يمكنهم التفاعل مع هذه الخصائص برمجيًا باستخدام[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).
### **تعيين الاتجاه والمحاذاة والهوامش ولون الخلفية والشفافية وموضع علامة التبويب الافتراضية للنص في قالب نص الشكل**
 يحتوي قسم تنسيق كتلة النص في ورقة الشكل Visio على معلومات التنسيق. ال[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) عروض الصف[كتلة النص](https://reference.aspose.com/diagram/java/com.aspose.diagram/TextBlock) للحصول على المظهر المرئي لنص الشكل أو تعيينه.
### **نموذج برمجة نص التنسيق**
يحدد الجزء التالي من التعليمات البرمجية الاتجاه والمحاذاة والهوامش ولون الخلفية وشفافية لون الخلفية وموضع علامة الجدولة الافتراضي لزاوية الاتجاه وموضع نص الشكل في الأعلى.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(FormatShapeTextBlockSection.class); 
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get the page by its name
Page page1 = diagram.getPages().getPage("Page-1");
// get shape by its ID
Shape shape = page1.getShapes().getShape(1);
// set orientation angle
DoubleValue margin = new DoubleValue(4, MeasureConst.PT);

// set left, right, top and bottom margins of the shape's text block
shape.getTextBlock().setLeftMargin(margin);
shape.getTextBlock().setRightMargin(margin);
shape.getTextBlock().setTopMargin(margin);
shape.getTextBlock().setBottomMargin(margin);

// set the text direction
shape.getTextBlock().getTextDirection().setValue(TextDirectionValue.VERTICAL);
// set the text alignment
shape.getTextBlock().getVerticalAlign().setValue(VerticalAlignValue.MIDDLE);
// set the text block background color
shape.getTextBlock().getTextBkgnd().getUfe().setF("RGB(95,108,53)");
// set the background color transparency in percent
shape.getTextBlock().getTextBkgndTrans().setValue(50);
// set the distance between default tab stops for the selected shape.
shape.getTextBlock().getDefaultTabStop().setValue(2);

// save Visio
diagram.save(dataDir + "FormatShapeTextBlockSection_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **قم بتدوير وتعيين موضع نص الشكل**
Aspose.Diagram API يسمح للمطورين بضبط موضع النص وأيضًا تدوير النص على الشكل Visio. لإنجاز هذه المهمة ، يوفر قسم تحويلات النص في ورقة الأشكال خصائص TxtPin و TxtLocPin و TxtWidth و TxtHeight. يمكن للمطورين التفاعل مع هذه الخصائص برمجيًا باستخدام Aspose.Diagram API.

يحتوي قسم تحويل النص على المعلومات الموضعية حول كتلة نص الشكل. توضح هذه الأمثلة كيفية ضبط مواضع نص الشكل وزاوية الاتجاه:

- [عيّن موضع نص الشكل في الأعلى](/diagram/ar/java/working-with-text-boxes/).
- [تعيين موضع نص الشكل في الأسفل](/diagram/ar/java/working-with-text-boxes/).
- [تعيين موضع نص الشكل إلى اليسار](/diagram/ar/java/working-with-text-boxes/).
- [اضبط موضع نص الشكل على اليمين](/diagram/ar/java/working-with-text-boxes/).
### **عيّن موضع نص الشكل في الأعلى**
يحدد الجزء التالي من التعليمات البرمجية زاوية الاتجاه وموضع نص الشكل في الأعلى.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetShapeTextPositionAtTop.class);   
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get shape
long shapeid = 1;
Shape shape = diagram.getPages().getPage("Page-1").getShapes().getShape(shapeid);

	    // set text position at the top,
	    // TxtLocPinY = "TxtHeight*0" and TxtPinY = "Height*1"
	    shape.getTextXForm().getTxtLocPinY().setValue(0);
	    shape.getTextXForm().getTxtPinY().setValue(shape.getXForm().getHeight().getValue());
	
	    // set orientation angle
	    double angleDeg = 0;
	    double angleRad = (Math.PI / 180) * angleDeg;
	    shape.getTextXForm().getTxtAngle().setValue(angleRad);

// save Visio diagram in the local storage
diagram.save(dataDir + "SetShapeTextPositionAtTop_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
### **تعيين موضع نص الشكل في الأسفل**
يحدد جزء الكود التالي زاوية الاتجاه وموضع نص الشكل في الأسفل.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetShapeTextPositionAtBottom.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get shape
long shapeid = 1;
Shape shape = diagram.getPages().getPage("Page-1").getShapes().getShape(shapeid);

	     // set text position at the bottom,
	     // TxtLocPinY = "TxtHeight*1" and TxtPinY = "Height*0"
	     shape.getTextXForm().getTxtLocPinY().setValue(shape.getTextXForm().getTxtHeight().getValue());
	     shape.getTextXForm().getTxtPinY().setValue(0);
	
	     // set orientation angle
	     double angleDeg = 0;
	     double angleRad = (Math.PI / 180) * angleDeg;
	     shape.getTextXForm().getTxtAngle().setValue(angleRad);     

// save Visio diagram in the local storage
diagram.save(dataDir + "SetShapeTextPositionAtBottom_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
### **تعيين موضع نص الشكل إلى اليسار**
يحدد الجزء التالي من التعليمات البرمجية زاوية الاتجاه وموضع نص الشكل على اليسار.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetShapeTextPositionAtLeft.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get shape
long shapeid = 1;
Shape shape = diagram.getPages().getPage("Page-1").getShapes().getShape(shapeid);

// set text position at the left,
// TxtLocPinX = "TxtWidth*1" and TxtPinX = "Width*0"
shape.getTextXForm().getTxtLocPinX().setValue(shape.getTextXForm().getTxtWidth().getValue());
shape.getTextXForm().getTxtPinX().setValue(0);
// set orientation angle
double angleDeg = 0;
double angleRad = (Math.PI / 180) * angleDeg;
shape.getTextXForm().getTxtAngle().setValue(angleRad);
        
// save Visio diagram in the local storage
diagram.save(dataDir + "SetShapeTextPositionAtLeft_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
### **اضبط موضع نص الشكل على اليمين**
يحدد الجزء التالي من التعليمات البرمجية زاوية الاتجاه وموضع نص الشكل على اليمين.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetShapeTextPositionAtRight.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get shape
long shapeid = 1;
Shape shape = diagram.getPages().getPage("Page-1").getShapes().getShape(shapeid);

// set text position at the right,
// TxtLocPinX = "TxtWidth*0" and TxtPinX = "Width*1"
shape.getTextXForm().getTxtLocPinX().setValue(0);
shape.getTextXForm().getTxtPinX().setValue(shape.getXForm().getWidth().getValue());
// set orientation angle
double angleDeg = 0;
double angleRad = (Math.PI / 180) * angleDeg;
shape.getTextXForm().getTxtAngle().setValue(angleRad);
        
// save Visio diagram in the local storage
diagram.save(dataDir + "SetShapeTextPositionAtRight_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
