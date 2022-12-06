---
title: 旋转、改变位置和连接子形状
type: docs
weight: 30
url: /zh/net/rotate-change-the-position-and-connect-sub-shapes/
description: 本节介绍如何使用 Aspose.Diagram 旋转 visio 形状。
---
## **以合适的角度旋转形状**
Aspose.Diagram for .NET 允许您将形状旋转到任意角度。公开的 SetAngle 方法[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类可用于将形状旋转到任何所需的角度。它采用单个参数作为角度。
### **旋转形状编程样本**
在您的 .NET 应用程序中使用以下代码来旋转使用 Aspose.Diagram for .NET 的形状。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-RotateVisioShape-RotateVisioShape.cs" >}}
## **更改形状的位置**
这[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类允许您更改形状的位置。当形状移动到不同位置时，连接线会自动调整。 Move 和 MoveTo 方法，由[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类，支持改变形状的位置作为组的一部分或不。本文中的代码示例在页面上移动一个形状。

移动形状的过程是：

1. 加载一个 diagram。
1. 找到一个特定的形状。
1. 将形状移动到不同的位置
1. 保存 diagram。
### **改变位置编程示例**
下面的代码片段显示了如何移动形状。该代码通过 ID 16 的名称和形状检索 Visio 页面，并移动其位置。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-MoveVisioShape-MoveVisioShape.cs" >}}
## **连接组的子形状**
本主题详细说明如何使用 Aspose.Diagram for .NET 连接 Microsoft Visio 图中两个不同组形状的两个子形状。[页](http://www.aspose.com/api/net/diagram/aspose.diagram/page)类可用于通过 ID 连接形状。 AddShape 方法，由[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)类，可用于添加形状。

下面的代码显示了如何：

1. 加载示例文件。
1. 访问特定页面。
1. 将动态连接器形状添加到所选页面。
1. 连接子形状
### **连接子形状编程示例**
在您的 .NET 应用程序中使用以下代码，使用 Aspose.Diagram for .NET 连接两个不同组形状的子形状。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-ConnectVisioSubShapes-ConnectVisioSubShapes.cs" >}}
## **获取连接到特定形状的形状**
[添加和连接 Visio 形状](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/)使用 Aspose.Diagram for .NET 说明如何添加形状并将其连接到 Microsoft Visio 图中的其他形状。也可以找到连接到特定形状的形状。

所公开的 ConnectedShapes 方法[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类可用于获取连接到形状的形状的 ID。 GetShape 方法，由[形状集合](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection)类，然后可用于通过其 ID 查找形状。

下面的代码显示了如何：

1. 加载示例文件。
1. 访问特定形状。
1. 获取连接到所选形状的所有形状的名称。
### **获取形状编程示例**
在您的 .NET 应用程序中使用以下代码，使用 Aspose.Diagram for .NET 查找连接到特定形状的所有形状。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-GetAllConnectedShapes-GetAllConnectedShapes.cs" >}}
