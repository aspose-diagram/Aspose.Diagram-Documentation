---
title: 修改Visio形状的渐变
type: docs
weight: 10
url: /zh/net/modify-the-gradient-of-a-visio-shape/
description: 本页介绍如何使用 Aspose.Diagram 库修改 visio 形状的渐变颜色。
---
{{% alert color="primary" %}} 

使用 Aspose.Diagram API，开发人员可以通过修改渐变的属性来增强 Visio 形状的外观。开发者可以检索一个渐变填充来设置方向、角度、渐变停止颜色和位置等。

{{% /alert %}} 
## **修改渐变填充编程示例**
[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类提供 Fill 属性，允许开发人员检索[渐变填充](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientfill)目的。 GradientFill 类保存了一个 Visio Shape 的渐变数据。开发人员可以设置其所有可用属性以及通过索引检索渐变停止以设置颜色和位置属性。

```
{{< highlight "csharp" >}}
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeGradientFillData();
// Load the Visio diagram
Diagram diagram = new Diagram(dataDir + "ShapewithGradientFill.vsdx");
// get page by name
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");
// get shape by ID
Aspose.Diagram.Shape shape = page.Shapes.GetShape(1);
// get the gradient fill properties
GradientFill gradientfill = shape.Fill.GradientFill;
// get the gradient stops
GradientStopCollection stops = gradientfill.GradientStops;
// get the gradient stop by index
GradientStop stop = stops[0];
// set gradient stop properties
stop.Color.Ufe.F = "";
stop.Position.Value = 0.5;
gradientfill.GradientDir.Value = (int)GradientFillDir.RectangleFromBottomRight;
gradientfill.GradientAngle.Value = 0.7853981633974501;
// save the Visio drawing
diagram.Save(dataDir + "ShapewithGradientFill_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
