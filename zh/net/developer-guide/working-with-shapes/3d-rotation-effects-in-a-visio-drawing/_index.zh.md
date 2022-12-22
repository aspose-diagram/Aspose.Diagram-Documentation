---
title: Visio 绘图中的 3D 旋转效果
type: docs
weight: 90
url: /zh/net/3d-rotation-effects-in-a-visio-drawing/
description: 本节介绍如何使用 Aspose.Diagram 在 Shapesheet 中设置 3D 旋转属性。
---
## **在形状表中设置 3D 旋转属性**
Aspose.Diagram API 允许开发人员更改形状表中的 3D 旋转值。 RotationXAngle、RotationYAngle 和 RotationZAngle 单元格值控制每个相应轴的旋转度数。 RotationType 的枚举值控制旋转类型：

1. 平行旋转，在不考虑线性透视的情况下旋转形状。
1. 透视旋转，其中形状以线性透视旋转。
1. 倾斜旋转预设（左下、右下、左上和右上），其中形状通过倾斜投影旋转。

这**保持文字平整**单元格值指示形状的文本是否将忽略形状在 3-D 中的旋转。它不适用于二维旋转。这**离地距离**单元格值确定对象在 3-D 中旋转时从点中的地面升高的距离。这**看法**单元格值确定透视旋转的透视角度，以度为单位（0 到 359.9）。
### **设置 3D 旋转属性**
暴露的 ThreeDFormat 成员[形状](https://reference.aspose.com/diagram/net/aspose.diagram/shape)类可用于设置 3d 旋转属性。

下面的代码显示了如何：

1. 加载源图形。
1. 按页面名称和 ID 参数检索形状。
1. 设置 3D 旋转属性。
1. 保存图纸
#### **3D 旋转编程示例**
在您的 .NET 应用程序中使用以下代码使用 Aspose.Diagram for .NET API 设置 3D 旋转属性。

**.NET, C#**

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram(@"c:\temp\TestTemplate.vsdx");

// get shape by ID and page name

Shape shape = diagram.Pages.GetPage("Page-1").Shapes.GetShape(0);



// set 3D rotation properties

shape.ThreeDFormat.RotationXAngle.Value = 2.61;

shape.ThreeDFormat.RotationYAngle.Value = 2.61;

shape.ThreeDFormat.RotationZAngle.Value = 3;

shape.ThreeDFormat.RotationType.Value = RotationTypeValue.ObliqueFromBottomLeft;

shape.ThreeDFormat.Perspective.Value = 0;

shape.ThreeDFormat.DistanceFromGround.Value = 0;

shape.ThreeDFormat.KeepTextFlat.Value = BOOL.True;

// save drawing

diagram.Save(@"c:\temp\TestTemplate.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
