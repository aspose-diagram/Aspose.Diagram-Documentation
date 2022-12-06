---
title: 设置 Visio Shape 的 XForm、Line 和 Fill 数据
type: docs
weight: 20
url: /zh/net/set-visio-shape-s-xform-line-and-fill-data/
description: 本节介绍如何设置形状的样式，包括它的线数据和填充数据 Aspose.Diagram。
---
## **设置变形数据**
XForm 元素是 Microsoft Visio XML 模式的一部分。 XForm 指定形状位置，例如宽度、高度、旋转以及形状是否已翻转。这[变形](http://www.aspose.com/api/net/diagram/aspose.diagram/xform)财产，由暴露[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类，支持 Aspose.Diagram.XForm 对象。 XForm 属性可用于检索或更新形状的 XForm 数据。本文中的代码示例更改 PinX（X 坐标）和 PinY（Y 坐标）XForm 值以移动页面上的形状。

更新 XForm 数据的过程是：

1. 加载 diagram。# 查找特定形状。# 更新形状的 XForm 数据。
1. 保存 diagram。
### **编程范例**
下面的代码片段显示了如何更新形状的 XForm 数据。代码查找形状名称进程，形状 ID 为 1，并将其 X 和 Y 坐标设置为 5。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SetXFormdata-SetXFormdata.cs" >}}
## **设置 Visio 形状的线数据**
可以通过多种方式格式化形状。本文介绍如何指定线条的属性。

Microsoft Visio 允许用户以各种方式格式化行。 Aspose.Diagram for .NET 支持：

- 权重：一条线的粗细。
- 颜色：设置形状的线条颜色。
- 线条颜色透明度：以百分比设置形状的线条颜色透明度。
- 图案：定义线条是实线、虚线还是其他图案。
- 圆角：角的半径。
- 开始和结束箭头：指定行是否有箭头。
- 开始和结束箭头大小：设置箭头大小。
- Cap：线的圆角结束。
### **更改形状边框的线条颜色、粗细、破折号类型、透明度、圆角、箭头类型和箭头大小**
这[线](http://www.aspose.com/api/net/diagram/aspose.diagram/line)财产，由暴露[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类，支持 Aspose.Diagram.Line 对象。此属性可用于检索或更新形状的线条数据。
#### **线路数据编程示例**
下面的一段代码更新形状的线数据。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SetLineData-SetLineData.cs" >}}
## **设置 Visio 形状的填充数据**
可以通过多种方式格式化形状。本主题介绍如何指定形状的填充。 Microsoft Office Visio 允许用户以各种方式填写格式。这[充满](http://www.aspose.com/api/net/diagram/aspose.diagram/fill)Aspose.Diagram for .NET API 类支持设置：

- 背景和前景色。
- 透明度。
- 填充图案。
- 阴影。
### **设置填充值**
Fill 属性，由[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类，支持[Aspose.Diagram.Fill](http://www.aspose.com/api/net/diagram/aspose.diagram/fill)目的。 Fill 属性可用于检索或更新形状的填充数据。
#### **填充数据编程示例**
以下代码片段更新形状的填充数据。该代码查找名为 rectangle 且形状 ID 为 1 的形状，并设置填充背景和前景色。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SetFillData-SetFillData.cs" >}}
### **检索 Visio 形状的继承填充数据**
 Visio 形状可以继承父样式和主形状。开发者可以获取或设置一个Visio形状的继承填充数据。 InheritFill 属性，由[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类，包含由父样式和主控形状继承的形状的填充格式值。
#### **检索继承的填充数据编程示例**
以下代码片段检索形状的继承填充数据。请检查此示例代码：

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RetrieveInheritedFillData-RetrieveInheritedFillData.cs" >}}
