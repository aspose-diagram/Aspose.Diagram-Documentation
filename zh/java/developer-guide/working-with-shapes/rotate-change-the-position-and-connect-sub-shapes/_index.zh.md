﻿---
title: 旋转、改变位置和连接子形状
type: docs
weight: 60
url: /zh/java/rotate-change-the-position-and-connect-sub-shapes/
---
## **以合适的角度旋转形状**
Aspose.Diagram for Java 允许您将形状旋转到任意角度。公开的 SetAngle 方法[形状](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)类可用于将形状旋转到任何所需的角度。它采用单个参数作为角度。
### **旋转形状编程样本**
在您的 Java 应用程序中使用以下代码来旋转使用 Aspose.Diagram for Java 的形状。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RotateVisioShape-RotateVisioShape.java" >}}
## **更改形状的位置**
Shape 类允许您更改形状的位置。当形状移动到不同位置时，连接线会自动调整。

Shape 类公开的 Move 和 MoveTo 方法支持将形状的位置更改为组的一部分或不更改。
本文中的代码示例在页面上移动一个形状。
**输入 diagram** 

![待办事项：图片_替代_文本](http://i.imgur.com/cThgWnB.png)


**形状移动后的diagram** 

![待办事项：图片_替代_文本](http://i.imgur.com/Q3QByqe.png)

移动形状的过程是：

1. 加载一个 diagram。
1. 找到一个特定的形状。
1. 将形状移动到不同的位置
1. 保存 diagram。
### **改变位置编程示例**
下面的代码片段显示了如何移动形状。该代码通过 ID 16 的名称和形状检索 Visio 页面，并移动其位置。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-MoveVisioShape-MoveVisioShape.java" >}}
## **连接组的子形状**
本主题详细说明如何使用 Aspose.Diagram for Java 连接 Microsoft Visio 图中两个不同组形状的两个子形状。

 ConnectShapesViaConnector 方法由[页](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)类可用于通过 ID 连接形状。 AddShape 方法，由[Diagram](https://reference.aspose.com/diagram/java)类，可用于添加形状。

|<p>**输入diagram** </p><p>![待办事项：图片_替代_文本](http://i.imgur.com/74rDby5.png)</p>|<p>**子形状连接后的diagram** </p><p>![待办事项：图片_替代_文本](http://i.imgur.com/c387dZJ.png)</p>|
|:- |:- |
下面的代码显示了如何：

1. 加载示例文件。
1. 访问特定页面。
1. 将动态连接器形状添加到所选页面。
1. 连接子形状
### **连接子形状编程示例**
在您的 Java 应用程序中使用以下代码，使用 Aspose.Diagram for Java 连接两个不同组形状的子形状。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ConnectVisioSubShapes-ConnectVisioSubShapes.java" >}}
## **获取连接到特定形状的形状**
[添加和连接 Visio 形状](/diagram/zh/java/add-and-connect-visio-shapes/)使用 Aspose.Diagram for Java 说明如何添加形状并将其连接到 Microsoft Visio 图中的其他形状。也可以找到连接到特定形状的形状。

所公开的 ConnectedShapes 方法[形状](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)类可用于获取连接到形状的形状的 ID。 GetShape 方法，由[形状集合](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection)类，然后可用于通过其 ID 查找形状。

下面的代码显示了如何：

1. 加载示例文件。
1. 访问特定形状。
1. 获取连接到所选形状的所有形状的名称。
### **获取形状编程示例**
在您的 Java 应用程序中使用以下代码，使用 Aspose.Diagram for Java 查找连接到特定形状的所有形状。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-GetAllConnectedShapes-GetAllConnectedShapes.java" >}}
