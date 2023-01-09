---
title: 计算引脚值和设置形状的大小
type: docs
weight: 40
url: /zh/java/calculate-pin-values-and-setting-size-of-a-shape/
---
## **计算子形状的 PinX 和 PinY 值**
如果形状是组形状的孩子，它的 xform 是它的父形状的相对坐标，但不是绝对坐标[页](https://reference.aspose.com/diagram/java/com.aspose.diagram/page).如果用户需要获取绝对坐标，则此示例代码会有所帮助。

通过按以下顺序应用以下转换，可以将局部坐标中指定的点转换为父坐标：

1. 从 x 坐标中减去 Cell_Type 元素的 LocPinX 属性值。
1. 从 y 坐标中减去 Cell_Type 的 LocPinY 属性值。
1. 如果 Cell_Type 的 FlipX 属性的值等于 1，则镜像关于 y 轴的点。
1. 如果 Cell_Type 的 FlipY 属性的值等于 1，则镜像关于 x 轴的点。
1. 根据 Cell_Type 的 Angle 属性的值，围绕原点逆时针旋转该点。
1. 将 PinX Cell_Type 的值添加到 x 坐标。
1. 将 PinY Cell_Type 的值添加到 y 坐标。
### **计算 PinX 和 PinY 编程示例**
在您的 Java 应用程序中使用以下代码，使用 Aspose.Diagram for Java API 计算子形状的 PinX 和 PinY 值。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-CalculateCenterOfSubShapes-CalculateCenterOfSubShapes.java" >}}
## **设置形状的高度和宽度**
这[形状](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)类允许您通过使用 SetHeight 和 SetWidth 方法指定形状的高度和宽度来控制形状大小。

 SetHeight 和 SetWidth 方法，由[形状](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape)类，支持带母版、无母版或组形变大。

本文中的代码示例设置高度和宽度以调整页面上形状的大小。

**输入 diagram** 

![待办事项：图片_替代_文本](http://i.imgur.com/cTiNWa7.png)

**改变高度和宽度后的diagram**

![待办事项：图片_替代_文本](calculate-pin-values-and-setting-size-of-a-shape_1.png)

设置Height和Width的过程是：

1. 加载一个 diagram。
1. 找到一个特定的形状。
1. 设置形状的高度。
1. 设置形状的宽度。
1. 保存 diagram。
### **设置高度和宽度编程示例**
下面的代码片段显示了如何设置形状的高度和宽度。该代码查找形状名称为矩形且形状 ID 为 1 的矩形，并将其高度和宽度设置为双精度值。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ChangeShapeSize-ChangeShapeSize.java" >}}
