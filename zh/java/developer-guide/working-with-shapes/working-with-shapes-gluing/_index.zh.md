---
title: 使用形状粘合
type: docs
weight: 10
url: /zh/java/working-with-shapes-gluing/
---
## **将连接器粘合到特定形状**
[添加和连接 Visio 形状](/diagram/zh/java/add-and-connect-visio-shapes/)使用 Aspose.Diagram for Java 说明如何添加形状并将其连接到 Microsoft Visio 图中的其他形状。也可以找到粘附到此形状的连接器。
### **获得粘合形状**
公开的 GluedShapes 方法[形状](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)类可用于获取粘附到形状的所有连接器的 ID 列表，或者，如果所讨论的形状是连接器，则获取它所连接到的形状的 ID。GetShape 方法，由[形状集合](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection)类，然后可用于通过其 ID 查找形状。

下面的代码显示了如何：

1. 加载示例文件。
1. 访问特定形状。
1. 获取粘附到此形状的所有连接器的 ID 列表。
#### **获取连接器粘合编程示例**
在您的 Java 应用程序中使用以下代码来查找使用 Aspose.Diagram for Java 粘附到形状上的所有连接器。

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetGluedConnectors.class);   
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "RetrieveShapeInfo.vsd");
// get shape by an ID
Shape shape = diagram.getPages().get(0).getShapes().getShape(90);
// get all glued 1D shapes
long[] gluedShapeIds = shape.gluedShapes(GluedShapesFlags.GLUED_SHAPES_ALL_1_D, null, null);

// display shape ID and name
for (long id : gluedShapeIds)
{
    shape = diagram.getPages().get(0).getShapes().getShape(id);
    System.out.println("ID: " + shape.getID() + "\t\t Name: " + shape.getName());
}

{{< /highlight >}}
```
## **将 Visio 形状与连接点粘合在一起**
Aspose.Diagram for Java 允许开发人员通过连接点将形状粘合在一起。
### **胶水形状**
公开的 GlueShapes 方法[页](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)类可以使用。

|<p>**输入 diagram** </p><p>![待办事项：图片_替代_文本](http://i.imgur.com/Z69f4hg.png)</p>|<p>**粘合形状后的 diagram** </p><p>![待办事项：图片_替代_文本](http://i.imgur.com/5TJpDwc.png)</p>|
|:- |:- |
下面的代码显示了如何：

1. 加载示例文件。
1. 胶水形状。
1. 保存 diagram。
#### **胶水 Visio 形状编程示例**
在您的 Java 应用程序中使用以下代码通过连接点粘合形状：

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GlueVisioShapes.class);
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.getPages().getPage("Page-1");
// set shape id
long shape1_ID = 7;
long shape2_ID = 494;
// Glue shapes
page.glueShapes(shape1_ID, ConnectionPointPlace.CENTER, shape2_ID);

// Save diagram
diagram.save(dataDir + "GlueVisioShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **在容器内粘贴形状**
Aspose.Diagram for Java 使开发人员能够将组形状粘附在容器内。
### **胶团形状**
可以使用 Page 类公开的 GlueShapesInContainer 方法。

|<p>**输入 diagram** </p><p>![待办事项：图片_替代_文本](http://i.imgur.com/HRRzIEh.png)</p>|<p>**粘合组形状后的diagram** </p><p>![待办事项：图片_替代_文本](http://i.imgur.com/YxCiOgU.png)</p>|
|:- |:- |
下面的代码显示了如何：

1. 加载示例文件。
1. 胶组形状。
1. 保存 diagram。
#### **编程示例中的胶水形状**
在 Java 应用程序中使用以下代码将组形状粘附在容器内：

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GlueContainerShape.class);   
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.getPages().getPage("Page-1");

// The ID of shape which is glue from Aspose.Diagram.Shape.
long shapeFromId = 779;
// The location on the first connection index where to glue
int shapeToBeginConnectionIndex = 72;
// The location on the end connection index where to glue
int shapeToEndConnectionIndex = 73;
// The ID of shape where to glue to Aspose.Diagram.Shape.
long shapeToId = 743;

// Glue shapes in container
page.glueShapesInContainer(shapeFromId, shapeToBeginConnectionIndex, shapeToEndConnectionIndex, shapeToId);

// Glue shapes in container using connection name
// page.GlueShapesInContainer(fasId, "U05L", "U05R", cabinetId1);

// Save diagram
diagram.save(dataDir + "GlueContainerShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
