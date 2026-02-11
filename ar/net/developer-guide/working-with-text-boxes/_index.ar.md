---
title: العمل مع مربعات النص
type: docs
weight: 210
url: /ar/net/working-with-text-boxes/
description: يوضح هذا القسم كيفية تنسيق شكل نص باستخدام Aspose.Diagram.
---
## **تنسيق النص في مقطع كتلة نص الشكل Visio**
 Aspose.Diagram API يسمح للمطورين بالتحكم في اتجاه النص والمحاذاة والهوامش ولون الخلفية وشفافية لون الخلفية وموضع إيقاف علامة الجدولة الافتراضي للنص في كتلة نص الشكل. يمكنهم التفاعل مع هذه الخصائص برمجيًا باستخدام[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **تعيين الاتجاه والمحاذاة والهوامش ولون الخلفية والشفافية وموضع علامة التبويب الافتراضية للنص في قالب نص الشكل**
 يحتوي قسم تنسيق كتلة النص في ورقة الشكل Visio على معلومات التنسيق. ال[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) عروض الصف[كتلة النص](http://www.aspose.com/api/net/diagram/aspose.diagram/textblock) للحصول على المظهر المرئي لنص الشكل أو تعيينه.
### **نموذج برمجة نص التنسيق**
يحدد الجزء التالي من التعليمات البرمجية الاتجاه والمحاذاة والهوامش ولون الخلفية وشفافية لون الخلفية وموضع علامة الجدولة الافتراضي لزاوية الاتجاه وموضع نص الشكل في الأعلى.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeTextBoxData();
            
// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get the page by its name
Aspose.Diagram.Page page1 = diagram.Pages.GetPage("Page-1");
// Get shape by its ID
Aspose.Diagram.Shape shape = page1.Shapes.GetShape(1);
// Set orientation angle
DoubleValue margin = new DoubleValue(4, MeasureConst.PT);

// Set left, right, top and bottom margins of the shape's text block
shape.TextBlock.LeftMargin = margin;
shape.TextBlock.RightMargin = margin;
shape.TextBlock.TopMargin = margin;
shape.TextBlock.BottomMargin = margin;
// Set the text direction
shape.TextBlock.TextDirection.Value = TextDirectionValue.Vertical;
// Set the text alignment
shape.TextBlock.VerticalAlign.Value = VerticalAlignValue.Middle;
// Set the text block background color
shape.TextBlock.TextBkgnd.Ufe.F = "RGB(95,108,53)";
// Set the background color transparency in percent
shape.TextBlock.TextBkgndTrans.Value = 50;
// Set the distance between default tab stops for the selected shape.
shape.TextBlock.DefaultTabStop.Value = 2;

// Save Visio
diagram.Save(dataDir + "FormatShapeTextBlockSection_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **تدوير وتعيين موضع Visio نص الشكل**
 Aspose.Diagram API يسمح للمطورين بضبط موضع النص وأيضًا تدوير النص على الشكل Visio. لإنجاز هذه المهمة ، يوفر قسم تحويلات النص في ورقة الأشكال خصائص TxtPin و TxtLocPin و TxtWidth و TxtHeight. يمكن للمطورين التفاعل مع هذه الخصائص برمجيًا باستخدام ملفات[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **قم بتدوير وتعيين موضع نص الشكل**
يحتوي قسم تحويل النص على المعلومات الموضعية حول كتلة نص الشكل. توضح الأمثلة أدناه كيفية ضبط مواضع نص الشكل وزاوية الاتجاه.
#### **عيّن موضع نص الشكل في الأعلى**
يحدد الجزء التالي من التعليمات البرمجية زاوية الاتجاه وموضع نص الشكل في الأعلى.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeTextBoxData();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get shape
long shapeid = 1;
Shape shape = diagram.Pages.GetPage("Page-1").Shapes.GetShape(shapeid);

// Set text position at the top,
// TxtLocPinY = "TxtHeight*0" and TxtPinY = "Height*1"
shape.TextXForm.TxtLocPinY.Value = 0;
shape.TextXForm.TxtPinY.Value = shape.XForm.Height.Value;

// Set orientation angle
double angleDeg = 0;
double angleRad = (Math.PI / 180) * angleDeg;
shape.TextXForm.TxtAngle.Value = angleRad;

// Save Visio diagram in the local storage
diagram.Save(dataDir + "SetShapeTextPositionAtTop_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
#### **تعيين موضع نص الشكل في الأسفل**
يحدد جزء الكود التالي زاوية الاتجاه وموضع نص الشكل في الأسفل.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeTextBoxData();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get shape
long shapeid = 1;
Shape shape = diagram.Pages.GetPage("Page-1").Shapes.GetShape(shapeid);

// Set text position at the bottom,
// TxtLocPinY = "TxtHeight*1" and TxtPinY = "Height*0"
shape.TextXForm.TxtLocPinY.Value = shape.TextXForm.TxtHeight.Value;
shape.TextXForm.TxtPinY.Value = 0;

// Set orientation angle
double angleDeg = 0;
double angleRad = (Math.PI / 180) * angleDeg;
shape.TextXForm.TxtAngle.Value = angleRad;

// Save Visio diagram in the local storage
diagram.Save(dataDir + "SetShapeTextPositionAtBottom_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
#### **تعيين موضع نص الشكل إلى اليسار**
يحدد الجزء التالي من التعليمات البرمجية زاوية الاتجاه وموضع نص الشكل على اليسار.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeTextBoxData();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get shape
long shapeid = 1;
Shape shape = diagram.Pages.GetPage("Page-1").Shapes.GetShape(shapeid);

// Set text position at the left,
// TxtLocPinX = "TxtWidth*1" and TxtPinX = "Width*0"
shape.TextXForm.TxtLocPinX.Value = shape.TextXForm.TxtWidth.Value;
shape.TextXForm.TxtPinX.Value = 0;
// Set orientation angle
double angleDeg = 0;
double angleRad = (Math.PI / 180) * angleDeg;
shape.TextXForm.TxtAngle.Value = angleRad;

// Save Visio diagram in the local storage
diagram.Save(dataDir + "SetShapeTextPositionAtLeft_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
#### **اضبط موضع نص الشكل على اليمين**
يحدد الجزء التالي من التعليمات البرمجية زاوية الاتجاه وموضع نص الشكل على اليمين.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeTextBoxData();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get shape
long shapeid = 1;
Shape shape = diagram.Pages.GetPage("Page-1").Shapes.GetShape(shapeid);

// Set text position at the right,
// TxtLocPinX = "TxtWidth*0" and TxtPinX = "Width*1"
shape.TextXForm.TxtLocPinX.Value = 0;
shape.TextXForm.TxtPinX.Value = shape.XForm.Width.Value;
// Set orientation angle
double angleDeg = 0;
double angleRad = (Math.PI / 180) * angleDeg;
shape.TextXForm.TxtAngle.Value = angleRad;

// Save Visio diagram in the local storage
diagram.Save(dataDir + "SetShapeTextPositionAtRight_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
