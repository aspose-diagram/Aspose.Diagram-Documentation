---
title: 使用 Visio 形状数据
type: docs
weight: 30
url: /zh/java/working-with-visio-shape-data/
---
## **在 Visio 中添加新形状**
Aspose.Diagram for Java 允许您以不同方式操作 Microsoft Visio 图表。您可以做的其中一件事是向图表添加新形状。 Aspose.Diagram for Java 可让您向 diagram 添加新形状。添加的形状也可以使用 Aspose.Diagram for Java 进行自定义。

本主题介绍如何向 diagram 添加新的矩形形状。

使用 Aspose.Diagram for Java 的 API 创建新的形状，然后将这些形状添加到 diagram 的形状集合中。

添加新形状：

1. **查找页面** 每个 Visio diagram 包含一个页面集合。开发人员可以通过页面 ID 或名称检索页面，并将所需页面存储在[页](https://reference.aspose.com/diagram//java/com.aspose.diagram/page)类对象。
1. **添加形状的要求大师** 每个 Visio diagram 包含一个大师的集合。开发人员可以从现有模板文件（通过直接路径或文件流）添加主控（通过 ID 或名称）。
1. **在 Visio diagram 中添加形状** 开发者可以在 Visio diagram 中按页面索引（从 0 开始）、主名称、PinX、PinY、高度（可选）和宽度（可选）放置新形状。
1. **设置形状属性** Diagram 类的 AddShape 方法返回形状 ID。开发者可以使用这个 ID 从 Visio diagram 中检索形状，然后设置它的属性，例如颜色、位置、对齐方式和文本。

|<p>**输入diagram** </p><p>![待办事项：图片_替代_文本](working-with-visio-shape-data_1.png)</p>|<p>**添加了形状的 diagram** </p><p>![待办事项：图片_替代_文本](working-with-visio-shape-data_2.png)</p>|
|:- |:- |
### **添加编程示例**
下面的代码片段显示了如何执行每个步骤。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-AddingNewShape-AddingNewShape.java" >}}

{{% alert color="primary" %}}

我们欢迎您的查询和建议[Aspose.Diagram论坛](https://forum.aspose.com/c/diagram/17).我们会及时回复。

{{% /alert %}}
## **检索形状信息**
[使用图表](/diagram/zh/java/working-with-diagrams/)说明如何创建图表、添加形状和连接器，以及如何检索有关 diagram 元素的信息，例如[页数](/diagram/zh/java/retrieve-get-copy-and-insert-a-page/), [大师](/diagram/zh/java/working-with-masters/) , 连接器和[字体](/diagram/zh/java/aspose-diagram-font-operations/).本文介绍如何检索有关 diagram 中形状的信息。

diagram 中的每个形状都有一个 ID 和一个名称。使用 Visio 编程时 ID 很重要：它是访问形状的主要方法。每个形状还保留有关其制作母版（模板）的信息。

一个[形状](https://reference.aspose.com/diagram//java/com.aspose.diagram/shape)是 Visio 绘图中的对象。 Page 类公开的 Shapes 属性支持 Aspose.Diagram.Shape 对象的集合。 Shapes 属性可用于检索有关形状的信息。

例如，在下面的控制台窗口中，您可以看到包含四个形状的 diagram 的信息输出：两个终止符、一个进程和一个动态连接器。每个都有一个唯一的 ID 以及主（模板）形状的名称。

**显示形状信息的控制台窗口**

![待办事项：图片_替代_文本](working-with-visio-shape-data_3.png)

要检索 Visio 页面信息：

1. 加载 diagram。
1. 设置一个 foreach 循环以遍历 diagram 中的所有形状。
1. 显示形状信息。
### **检索编程样本**
下面的一段代码从 Visio diagram 中检索形状信息。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RetrieveShapeInfo-RetrieveShapeInfo.java" >}}
## **从现有的 Visio 复制形状**
Aspose.Diagram for Java API 允许开发人员将形状从源 Visio 页面复制到新的 Visio diagram 页面。它还支持复制组形状。本文介绍如何从源 diagram 页面复制所有形状。

要复制形状，开发人员还应复制源 PageSheet 和源 Visio 主题以保留形状填充样式和其他格式属性。

这个例子的工作原理如下：

1. 加载源 Visio。
1. 初始化一个新的 Visio
1. 从源 Visio 添加母版和主题。
1. 从源 Visio 获取页面。
1. 将其 PageSheet 复制到新的 Visio 页面。
1. 遍历源 Visio 页面的形状。
1. 设置它的新 id 并添加到新的 Visio 页面。
1. 将新的 Visio 保存在本地存储中。
### **复制编程示例**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-CopyShape-CopyShape.java" >}}

{{% alert color="primary" %}}

我们欢迎您的查询和建议[Aspose.Diagram论坛](https://forum.aspose.com/c/diagram/17).我们会及时回复。

{{% /alert %}}
## **将 Visio Shape 复制到另一个 Shape 实例**
Shape 类的复制方法采用要克隆的形状实例。

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Shape newShape = new Shape();

// copy diagram

newShape.copy(diagram.getPages().get(0).getShapes().get(0));

newShape.setID(3);

newShape.getXForm().getPinX().setValue(1);

newShape.getXForm().getPinY().setValue(1);

{{< /highlight >}}
## **读取 Visio 形状数据**
 Shape 类公开的 Props 集合支持[Aspose.Diagram.Prop](https://reference.aspose.com/diagram//java/com.aspose.diagram/prop)目的。该属性可用于读取形状的数据（自定义属性）。
### **读取所有形状属性**
识别 Microsoft Visio 中的自定义属性：

1. 在 diagram 中，右键单击一个形状。
1. 选择**数据**， 然后**形状数据**从菜单中。
对话框中列出了任何现有属性。

|**形状的数据，如 Microsoft Visio 中所示。**|** |
|:- |:- |
|![待办事项：图片_替代_文本](http://i.imgur.com/2loM7b0.png)||


|**显示形状数据输出的控制台窗口。**|** |
|:- |:- |
|![待办事项：图片_替代_文本](http://i.imgur.com/kmAKNrx.png)||
#### **阅读编程示例**
下面的代码片段读取形状数据（自定义属性）。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ReadAllShapeProps-ReadAllShapeProps.java" >}}
### **按名称读取形状属性**
下面的代码片段按名称（自定义属性）读取形状属性。
#### **按名称读取编程示例**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ReadShapePropByName-ReadShapePropByName.java" >}}
## **使用连接索引连接形状**
Aspose.Diagram for Java API 已经允许开发人员在形状上添加新的连接点，开发人员现在可以使用连接索引连接形状。
### **使用连接索引连接形状**
Page 类公开的 connectShapesViaConnectorIndex 成员可用于使用连接索引连接形状。以下代码显示了如何连接形状：

1. 初始化一个新绘图。
1. 放置四个矩形
1. 添加两个额外的连接点，以便在底部边框线上有三个连接点
1. 使用动态连接器将每个底部连接的第一个形状连接到顶部的其他三个矩形形状
1. 保存图纸
#### **使用连接索引连接形状编程示例**
在您的 Java 应用程序中使用以下代码，使用连接索引与 Aspose.Diagram for Java API 连接形状。

**Java**

{{< highlight "java" >}}

 // initialize a new drawing

Diagram diagram = new Diagram();

// get page by index

Page page = diagram.getPages().get(0);

// add masters

String connectorMaster = "Dynamic connector", rectangle = "Rectangle";

int pageNumber = 0;

double width = 2, height = 2, pinX = 4.25, pinY = 9.5;

diagram.addMaster("C:\\temp\\Basic Shapes.vss", rectangle);

diagram.addMaster("C:\\temp\\Basic Shapes.vss", connectorMaster);

// add shapes

long shape1_ID = diagram.addShape(4.5, 7, rectangle, pageNumber);

long shape2_ID = diagram.addShape(2.25, 4.5, rectangle, pageNumber);

long shape3_ID = diagram.addShape(4.5, 4.5, rectangle, pageNumber);

long shape4_ID = diagram.addShape(6.75, 4.5, rectangle, pageNumber);

// get shapes by ID

Shape shape1 = page.getShapes().getShape(shape1_ID);

Shape shape2 = page.getShapes().getShape(shape2_ID);

Shape shape3 = page.getShapes().getShape(shape3_ID);

Shape shape4 = page.getShapes().getShape(shape4_ID);

// add two more connection points

Connection connection1 = new Connection();

connection1.getX().getUfe().setF("Width*0.33");

connection1.getY().getUfe().setF("Height*0");

Connection connection3 = new Connection();

connection3.getX().getUfe().setF("Width*0.66");

connection3.getY().getUfe().setF("Height*0");

shape1.getConnections().add(connection1);

shape1.getConnections().add(connection3);



// add connector shapes

Shape connector1 = new Shape();

Shape connector2 = new Shape();

Shape connector3 = new Shape();

long connecter1Id = diagram.addShape(connector1, connectorMaster, 0);

long connecter2Id = diagram.addShape(connector2, connectorMaster, 0);

long connecter3Id = diagram.addShape(connector3, connectorMaster, 0);

// connect shapes by index of conneecting points

page.connectShapesViaConnectorIndex(shape1.getID(), 6, shape2.getID(), 3, connecter1Id);

page.connectShapesViaConnectorIndex(shape1.getID(), 1, shape3.getID(), 3, connecter2Id);

page.connectShapesViaConnectorIndex(shape1.getID(), 7, shape4.getID(), 3, connecter3Id);

// save drawing

diagram.save("C:\\temp\\Drawing1_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **检索子形状的父形状**
Aspose.Diagram for Java 允许开发人员检索子形状的父形状。
### **获取父形状**
Shape 类提供 getParentShape 属性来检索父形状。
#### **获取父形状编程示例**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RetrieveTheParentShape-RetrieveTheParentShape.java" >}}
