---
title: 计算引脚值和设置形状的大小
type: docs
weight: 60
url: /zh/net/calculate-pin-values-and-setting-size-of-a-shape/
description: 本节介绍如何使用 Aspose.Diagram 计算子形状的 PinX 和 PinY 值。
---
## **计算子形状的 PinX 和 PinY 值**
如果形状是组形状的子节点，则其 xform 是其父形状的相对坐标，而不是绝对坐标[页](http://www.aspose.com/api/net/diagram/aspose.diagram/page).如果用户需要获取绝对坐标，则此示例代码会有所帮助。

通过按以下顺序应用以下转换，可以将局部坐标中指定的点转换为父坐标：

1. 从 x 坐标中减去 Cell_Type 元素的 LocPinX 属性值。
1. 从 y 坐标中减去 Cell_Type 的 LocPinY 属性值。
1. 如果 Cell_Type 的 FlipX 属性的值等于 1，则镜像关于 y 轴的点。
1. 如果 Cell_Type 的 FlipY 属性的值等于 1，则镜像关于 x 轴的点。
1. 根据 Cell_Type 的 Angle 属性的值，围绕原点逆时针旋转该点。
1. 将 PinX Cell_Type 的值添加到 x 坐标。
1. 将 PinY Cell_Type 的值添加到 y 坐标。
### **计算 PinX 和 PinY 编程示例**
在您的 .NET 应用程序中使用以下代码，使用 Aspose.Diagram for .NET API 计算子形状的 PinX 和 PinY 值。








{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a group shape by ID and page index is 0
Shape shape = diagram.Pages[0].Shapes.GetShape(795);
// Get a sub-shape of the group shape by id
Shape subShape = shape.Shapes.GetShape(794);

Matrix m = new Matrix();
// Apply the translation vector
m.Translate(-(float)subShape.XForm.LocPinX.Value, -(float)subShape.XForm.LocPinY.Value);
// Set the elements of that matrix to a rotation
m.Rotate((float)subShape.XForm.Angle.Value);
// Apply the translation vector
m.Translate((float)subShape.XForm.PinX.Value, (float)subShape.XForm.PinY.Value);

// Get pinx and piny
double pinx = m.OffsetX;
double piny = m.OffsetY;
// Calculate the sub-shape pinx and piny
double resultx = shape.XForm.PinX.Value - shape.XForm.LocPinX.Value - pinx;
double resulty = shape.XForm.PinY.Value - shape.XForm.LocPinY.Value - piny;

{{< /highlight >}}

## **设置形状的高度和宽度**
这[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类允许您通过使用 SetHeight 和 SetWidth 方法指定形状的高度和宽度来控制形状大小。

 SetHeight 和 SetWidth 方法，由[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类，支持带母版、无母版或组形变大。本文中的代码示例设置高度和宽度以调整页面上形状的大小。

设置Height和Width的过程是：

1. 加载一个 diagram。
1. 找到一个特定的形状。
1. 设置形状的高度。
1. 设置形状的宽度。
1. 保存 diagram。
### **设置高度和宽度编程示例**
下面的代码片段显示了如何设置形状的高度和宽度。该代码查找形状名称为矩形且形状 ID 为 1 的矩形，并将其高度和宽度设置为双精度值。


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by id
Shape shape = page.Shapes.GetShape(796);
// Alter the size of Shape
shape.SetWidth(2 * shape.XForm.Width.Value);
shape.SetHeight(2 * shape.XForm.Height.Value);
// Save diagram
diagram.Save(dataDir + "ChangeShapeSize_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

