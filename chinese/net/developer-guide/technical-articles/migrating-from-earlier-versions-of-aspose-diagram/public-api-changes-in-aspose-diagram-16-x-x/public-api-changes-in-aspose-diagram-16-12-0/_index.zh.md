---
title: 公共 API Aspose.Diagram 16.12.0 的变化
type: docs
weight: 10
url: /zh/net/public-api-changes-in-aspose-diagram-16-12-0/
---
{{% alert color="primary" %}} 

本文档描述了 Aspose.Diagram API 从版本 16.11.0 到 16.12.0 的变化，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对 Aspose.Diagram 中幕后行为的任何更改的描述。

{{% /alert %}} 
## **修改渐变的属性**
开发人员可以检索梯度停止点，然后修改其属性。我们添加了[渐变填充](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientfill)和[梯度停止](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientstop)为此目的的课程。请检查代码示例：

**C#**

{{< highlight "csharp" >}}

 // load a Visio drawing

Diagram diagram = new Diagram(@"C:\temp\MyVisio.vsdx");

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

diagram.Save(@"C:\temp\Output.pdf", SaveFileFormat.PDF);

{{< /highlight >}}
