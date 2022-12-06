---
title: 分组、转换和验证形状
type: docs
weight: 80
url: /zh/net/group-convert-and-verify-shapes/
description: 本节介绍如何使用 Aspose.Diagram 对形状进行分组。
---
## **在 Visio 绘图中将多个形状组合在一起**
Aspose.Diagram API 允许开发人员将形状分组在一起以一次移动它们。组中的每个形状都保持唯一的身份并具有自己的一组属性。当我们更改一组形状的格式时，它会将新属性分配给每个形状。
### **如何对形状进行分组**
暴露的组方法[形状集合](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection)类可用于将形状组合在一起。

下面的代码显示了如何：

1. 加载示例 diagram。
1. 初始化形状数组
1. 通过 id 获取特定形状。
1. 通过 id 获得另一个特定的特定形状。
1. 将形状分配给数组。
1. 通过调用 Group 方法对形状进行分组。
1. 保存 diagram
#### **组形状编程示例**
在 .NET 应用程序中使用以下代码，使用 Aspose.Diagram for .NET API 将形状组合在一起。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-GroupShapes-GroupShapes.cs" >}}
## **将 Visio 形状转换为其他文件格式**
Aspose.Diagram for .NET API 允许开发人员将单个 Visio 形状转换为任何其他支持的文件格式。在本文中，我们从页面中删除所有其他 Visio 形状，并根据源形状大小自定义页面设置。
### **转换特定的 Visio 形状**
Developers can convert a Visio shape to PDF, HTML, Image, SVG, and SWF by **指定 Visio 保存选项**.
此示例代码的工作方式如下：

1. 加载源 Visio。
1. 获取特定页面。
1. 删除背景页面。
1. 构建一个包含所有形状的哈希表，其中包含 ID 和名称。
1. 遍历哈希表
1. 从 Visio 页面中删除所有形状，特定形状除外。
1. 设置页面大小。
1. 以任何支持的文件格式保存 Visio 页面。
#### **转换形状编程示例**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SaveVisioShapeInOtherFormats-SaveVisioShapeInOtherFormats.cs" >}}
### **Convert Visio Shape to PDF**
The ToPdf method of the Shape class allows to convert a shape into the PDF format.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Convert Visio Shape to HTML**
The ToHTML method of the Shape class allows to convert a shape into the HTML format.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}
## **验证两个 Visio 形状是否连接或粘合**
Aspose.Diagram for .NET API 允许开发人员验证两个 Visio 形状是否粘合或连接。之前，我们在这些帮助主题中看到了如何连接或粘合两个形状：[添加和连接 Visio 形状](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/)和[在容器内粘贴形状](/diagram/zh/net/working-with-shapes-gluing/).
### **连接或粘合形状的验证**
这[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类提供 IsGlued 和 IsConnected 属性来确定两个形状是粘合还是连接。
#### **连接或粘合形状编程示例的验证**
下面的一段代码验证两个形状是否连接或粘合。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-VerifyConnectedOrGluedShapes-VerifyConnectedOrGluedShapes.cs" >}}
## **验证 Visio 形状是否在一组形状中**
Aspose.Diagram for .NET API 允许开发人员验证 Visio 形状是否在一组形状中。
### **形状组中形状的验证**
这[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类提供 IsInGroup 属性来确定 Visio 形状是否在组形状中。
#### **形状组编程样本中形状的验证**
以下代码验证形状是否为组形状。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-VerifyShapeIsInGroup-VerifyShapeIsInGroup.cs" >}}
