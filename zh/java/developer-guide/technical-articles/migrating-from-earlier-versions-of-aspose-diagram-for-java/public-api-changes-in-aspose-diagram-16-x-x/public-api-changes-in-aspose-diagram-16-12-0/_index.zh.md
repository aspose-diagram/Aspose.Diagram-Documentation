---
title: 公共 API Aspose.Diagram 16.12.0 的变化
type: docs
weight: 10
url: /zh/java/public-api-changes-in-aspose-diagram-16-12-0/
---
{{% alert color="primary" %}} 

本文档描述了 Aspose.Diagram API 从版本 16.11.0 到 16.12.0 的变化，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对 Aspose.Diagram 中幕后行为的任何更改的描述。

{{% /alert %}} 
### **修改渐变的属性**
开发人员可以检索梯度停止点，然后修改其属性。我们添加了[渐变填充](https://reference.aspose.com/diagram/java/com.aspose.diagram/gradientfill)和[梯度停止](https://reference.aspose.com/diagram/java/com.aspose.diagram/gradientstop)为此目的的课程。请检查代码示例：

**Java**

{{< highlight "csharp" >}}

 // load a Visio drawing

Diagram diagram = new Diagram("C:\\temp\\MyVisio.vsdx");

// get page by name

Page page = diagram.getPages().getPage("Page-1");

// get shape by ID

Shape shape = page.getShapes().getShape(1);

// get the gradient fill properties

GradientFill gradientfill = shape.getFill().getGradientFill();

// get the gradient stops

GradientStopCollection stops = gradientfill.getGradientStops();

// get the gradient stop by index

GradientStop stop = stops.get(0);

// set gradient stop properties

stop.getColor().getUfe().setF("");

stop.getPosition().setValue(0.5);

gradientfill.getGradientDir().setValue(GradientFillDir.RECTANGLE_FROM_BOTTOM_RIGHT);

gradientfill.getGradientAngle().setValue(0.7853981633974501);

// save the Visio drawing

diagram.save("C:\\temp\\Output.pdf", SaveFileFormat.PDF);

{{< /highlight >}}
