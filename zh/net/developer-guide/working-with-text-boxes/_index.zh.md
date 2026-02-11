---
title: 使用文本框
type: docs
weight: 210
url: /zh/net/working-with-text-boxes/
description: 本节介绍如何使用 Aspose.Diagram 格式化文本形状。
---
## **在 Visio 形状的文本块部分设置文本格式**
Aspose.Diagram API 允许开发人员控制文本方向、对齐方式、边距、背景颜色、背景颜色透明度以及形状文本块中文本的默认制表位位置。他们可以使用编程方式与这些属性交互[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **设置形状文本块中文本的方向、对齐方式、边距、背景颜色、透明度和默认制表位**
 Visio 形状表的文本块格式部分包含格式信息。这[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)课程优惠[文本块](http://www.aspose.com/api/net/diagram/aspose.diagram/textblock)属性以获取或设置形状文本的视觉外观。
### **格式文本编程示例**
以下代码段设置方向、对齐方式、边距、背景颜色、背景颜色透明度以及方向角的默认制表位位置和形状文本在顶部的位置。


{{< highlight csharp >}}
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

## **旋转和设置 Visio 形状文本的位置**
Aspose.Diagram API 允许开发人员调整文本位置并旋转 Visio 形状上的文本。为完成此任务，形状表上的文本转换部分提供了 TxtPin、TxtLocPin、TxtWidth 和 TxtHeight 属性。开发人员可以使用以下方式以编程方式与这些属性进行交互[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **旋转和设置形状文本的位置**
文本转换部分包含有关形状文本块的位置信息。下面的示例显示了如何调整形状文本位置和方向角度。
#### **将形状的文本位置设置在顶部**
以下代码段设置形状文本在顶部的方向角度和位置。


{{< highlight csharp >}}
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

#### **将形状的文本位置设置在底部**
以下代码段设置形状文本在底部的方向角度和位置。


{{< highlight csharp >}}
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

#### **将形状的文本位置设置在左侧**
以下代码段设置形状文本在左侧的方向角度和位置。


{{< highlight csharp >}}
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

#### **将形状的文本位置设置在右侧**
以下代码段设置形状文本在右侧的方向角度和位置。


{{< highlight csharp >}}
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

