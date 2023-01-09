---
title: 使用形状粘合
type: docs
weight: 40
url: /zh/net/working-with-shapes-gluing/
description: 本节介绍如何使用 Aspose.Diagram 获取粘附到特定形状的形状。
---
## **将连接器粘合到特定形状**
[添加和连接 Visio 形状](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/)使用 Aspose.Diagram for .NET 说明如何添加形状并将其连接到 Microsoft Visio 图中的其他形状。也可以找到粘附到此形状的连接器。
### **获得粘合形状**
公开的 GluedShapes 方法[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类可用于获取粘附到形状的所有连接器的 ID 列表，或者，如果所讨论的形状是连接器，则获取它所连接到的形状的 ID。GetShape 方法，由[形状集合](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection)类，然后可用于通过其 ID 查找形状。

下面的代码显示了如何：

1. 加载示例文件。
1. 访问特定形状。
1. 获取粘附到此形状的所有连接器的 ID 列表。
#### **获取连接器粘合编程示例**
在您的 .NET 应用程序中使用以下代码来查找使用 Aspose.Diagram for .NET 粘附到形状上的所有连接器。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Shapes-Gluing-GetGluedConnectors-GetGluedConnectors.cs" >}}
## **将 Visio 形状与连接点粘合在一起**
Aspose.Diagram for .NET 允许开发人员通过连接点将形状粘合在一起。
### **胶水形状**
公开的 GlueShapes 方法[页](http://www.aspose.com/api/net/diagram/aspose.diagram/page)类可以使用。

|<p>**输入 diagram** </p><p>![待办事项：图片_替代_文本](working-with-shapes-gluing_1.png)</p>|<p>**粘合形状后的 diagram** </p><p>![待办事项：图片_替代_文本](working-with-shapes-gluing_2.png)</p>|
|:- |:- |
下面的代码显示了如何：

1. 加载示例文件。
1. 胶水形状。
1. 保存 diagram。
#### **胶水 Visio 形状编程示例**
在您的 .NET 应用程序中使用以下代码通过连接点粘合形状：

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Shapes-Gluing-GlueVisioShapes-GlueVisioShapes.cs" >}}
## **在容器内粘贴形状**
Aspose.Diagram for .NET 使开发人员能够将组形状粘附在容器内。
### **胶团形状**
公开的 GlueShapesInContainer 方法[页](http://www.aspose.com/api/net/diagram/aspose.diagram/page)类可以使用。

|<p>**输入 diagram** </p><p>![待办事项：图片_替代_文本](working-with-shapes-gluing_3.png)</p>|<p>**粘合组形状后的diagram** </p><p>![待办事项：图片_替代_文本](working-with-shapes-gluing_4.png)</p>|
|:- |:- |
下面的代码显示了如何：

1. 加载示例文件。
1. 胶组形状。
1. 保存 diagram。
#### **编程示例中的胶水形状**
在 .NET 应用程序中使用以下代码将组形状粘附在容器内：

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Shapes-Gluing-GlueContainerShape-GlueContainerShape.cs" >}}
