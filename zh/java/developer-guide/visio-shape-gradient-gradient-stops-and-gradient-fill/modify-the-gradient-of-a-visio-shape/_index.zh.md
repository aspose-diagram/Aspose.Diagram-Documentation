---
title: 修改Visio形状的渐变
type: docs
weight: 10
url: /zh/java/modify-the-gradient-of-a-visio-shape/
---
{{% alert color="primary" %}} 

使用 Aspose.Diagram API，开发人员可以通过修改渐变的属性来增强 Visio 形状的外观。开发者可以检索一个渐变填充来设置方向、角度、渐变停止颜色和位置等。

{{% /alert %}} 
## **修改渐变填充编程示例**
[形状](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)类提供 Fill 属性，允许开发人员检索[渐变填充](https://reference.aspose.com/diagram/java/com.aspose.diagram/gradientfill)目的。 GradientFill 类保存了一个 Visio Shape 的渐变数据。开发人员可以设置其所有可用属性以及通过索引检索渐变停止以设置颜色和位置属性。

```
{{< highlight "java" >}}
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(ModifyShapeGradientFill.class) + "ShapeGradientFill\\";

// load a Visio drawing
Diagram diagram = new Diagram(dataDir + "ShapewithGradientFill.vsdx");
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
diagram.save(dataDir + "ShapewithGradientFill_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}
```
