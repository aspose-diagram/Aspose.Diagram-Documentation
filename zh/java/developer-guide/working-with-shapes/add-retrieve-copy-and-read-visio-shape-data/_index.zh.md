---
title: 添加、检索、复制和读取 Visio 形状数据
type: docs
weight: 10
url: /zh/java/add-retrieve-copy-and-read-visio-shape-data/
description: 本节介绍如何添加形状、设置形状的属性或使用 Aspose.Diagram 复制形状。
---
## **在 Visio 中添加新形状**
Aspose.Diagram for Java 允许您以不同方式操作 Microsoft Visio 图表。您可以做的其中一件事是向图表添加新形状。 Aspose.Diagram for Java 可让您向 diagram 添加新形状。添加的形状也可以使用 Aspose.Diagram for Java 进行自定义。

本主题介绍如何向 diagram 添加新的矩形形状。

使用 Aspose.Diagram for Java API 创建新形状，然后将这些形状添加到 diagram 的形状集合中。

添加新形状：

1. **查找页面** 每个 Visio diagram 包含一个页面集合。开发人员可以通过页面 ID 或名称检索页面，并将所需页面存储在[页](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)类对象。
1. **添加形状的要求大师** 每个 Visio diagram 包含一个大师的集合。开发人员可以从现有模板文件（通过直接路径或文件流）添加主控（通过 ID 或名称）。
1. **在 Visio diagram 中添加形状** 开发者可以在 Visio diagram 中按页面索引（从 0 开始）、主名称、PinX、PinY、高度（可选）和宽度（可选）放置新形状。
1. **设置形状属性** Diagram 类的 AddShape 方法返回形状 ID。开发者可以使用这个 ID 从 Visio diagram 中检索形状，然后设置它的属性，例如颜色、位置、对齐方式和文本。

|<p>**输入diagram** </p><p>![待办事项：图片_替代_文本](add-retrieve-copy-and-read-visio-shape-data_1.png)</p>|<p>**添加了形状的 diagram** </p><p>![待办事项：图片_替代_文本](add-retrieve-copy-and-read-visio-shape-data_2.png)</p>|
|:- |:- |
### **添加编程示例**
下面的代码片段显示了如何执行每个步骤。


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddingNewShape.class);  
//Load a diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-2");

// Add master with stencil file path and master id
String masterName = "Rectangle";
// Add master with stencil file path and master name
diagram.addMaster(dataDir + "Basic Shapes.vss", masterName);
            
// page indexing starts from 0
int PageIndex = 1;
double width = 2, height = 2, pinX = 4.25, pinY = 4.5;
//Add a new rectangle shape
long rectangleId = diagram.addShape(pinX, pinY, width, height, masterName, PageIndex);
            
// set shape properties 
Shape rectangle = page.getShapes().getShape(rectangleId);
rectangle.getXForm().getPinX().setValue(5);
rectangle.getXForm().getPinY().setValue(5);
rectangle.setType(TypeValue.SHAPE);
rectangle.getText().getValue().add(new Txt("Aspose Diagram"));
rectangle.setTextStyle(diagram.getStyleSheets().get(3));
rectangle.getLine().getLineColor().setValue("#ff0000");
rectangle.getLine().getLineWeight().setValue(0.03);
rectangle.getLine().getRounding().setValue(0.1);
rectangle.getFill().getFillBkgnd().setValue("#ff00ff");
rectangle.getFill().getFillForegnd().setValue("#ebf8df");

diagram.save(dataDir + "AddShape_Out.vsdx", SaveFileFormat.VSDX);
System.out.println("Shape has been added.");

{{< /highlight >}}


{{% alert color="primary" %}}

我们欢迎您的查询和建议[Aspose.Diagram论坛](https://forum.aspose.com/c/diagram/17).我们会及时回复。

{{% /alert %}}
## **检索形状信息**
[使用图表](/diagram/zh/java/working-with-diagrams/)说明如何创建图表、添加形状和连接器，以及如何检索有关 diagram 元素的信息，例如[页数](/diagram/zh/java/retrieve-get-copy-and-insert-a-page/), [大师](https://docs.aspose.com/diagram/java/working-with-masters/), [连接器](https://reference.aspose.com/diagram/java/com.aspose.diagram/ConnectCollection)和[字体](https://reference.aspose.com/diagram/java/com.aspose.diagram/FontCollection).本文介绍如何检索有关 diagram 中形状的信息。

diagram 中的每个形状都有一个 ID 和一个名称。使用 Visio 编程时 ID 很重要：它是访问形状的主要方法。每个形状还保留有关其制作母版（模板）的信息。

一个[形状](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape)是 Visio 绘图中的对象。 Page 类公开的 Shapes 属性支持 Aspose.Diagram.Shape 对象的集合。 Shapes 属性可用于检索有关形状的信息。

例如，在下面的控制台窗口中，您可以看到包含四个形状的 diagram 的信息输出：两个终止符、一个进程和一个动态连接器。每个都有一个唯一的 ID 以及主（模板）形状的名称。

|**显示形状信息的控制台窗口**|
|:- |
|![待办事项：图片_替代_文本](add-retrieve-copy-and-read-visio-shape-data_3.png)|
要检索 Visio 页面信息：

1. 加载 diagram。
1. 设置一个 foreach 循环以遍历 diagram 中的所有形状。
1. 显示形状信息。
### **检索编程样本**
下面的一段代码从 Visio diagram 中检索形状信息。


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveShapeInfo.class);

//Load diagram
Diagram diagram = new Diagram(dataDir+ "RetrieveShapeInfo.vsd");

for (com.aspose.diagram.Shape shape : (Iterable<Shape>) diagram.getPages().getPage(0).getShapes())
{
    //Display information about the shapes
    System.out.println("\nShape ID : " + shape.getID());
    System.out.println("Name : " + shape.getName());
    System.out.println("Master Shape : " + shape.getMaster().getName());
}

{{< /highlight >}}


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

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CopyShape.class); 
// load a source Visio
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");
        
// initialize a new Visio
Diagram newDiagram = new Diagram();

// add all masters from the source Visio diagram
MasterCollection originalMasters = srcVisio.getMasters();
for (Master master : (Iterable<Master>) originalMasters)
    newDiagram.addMaster(srcVisio, master.getName());

// get the page object from the original diagram
Page SrcPage = srcVisio.getPages().getPage("Page-1");
// copy themes from the source diagram
newDiagram.copyTheme(srcVisio);
// copy pagesheet of the source Visio page
newDiagram.getPages().get(0).getPageSheet().copy(SrcPage.getPageSheet());

// copy shapes from the source Visio page
for (Shape shape :(Iterable<Shape>) SrcPage.getShapes())
{
    newDiagram.getPages().get(0).getShapes().add(shape);
}
// save the new Visio
newDiagram.save(dataDir + "CopyShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}



{{% alert color="primary" %}}

我们欢迎您的查询和建议[Aspose.Diagram论坛](https://forum.aspose.com/c/diagram/17).我们会及时回复。

{{% /alert %}}
## **将 Visio Shape 复制到另一个 Shape 实例**
Shape 类的 Copy 方法采用要克隆的形状实例。

## **读取 Visio 形状数据**
暴露的 Props 集合[形状](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape)类支持[Aspose.Diagram.Prop](http://www.aspose.com/api/java/diagram/com.aspose.diagram/prop)目的。该属性可用于读取形状的数据（自定义属性）。
### **读取所有形状属性**
识别 Microsoft Visio 中的自定义属性：

1. 在 diagram 中，右键单击一个形状。
1. 选择**数据**， 然后**形状数据**从菜单中。
对话框中列出了任何现有属性。

|**形状的数据，如 Microsoft Visio 中所示。**|** |
|:- |:- |
|![待办事项：图片_替代_文本](add-retrieve-copy-and-read-visio-shape-data_4.png)||


|**显示形状数据输出的控制台窗口。**|** |
|:- |:- |
|![待办事项：图片_替代_文本](add-retrieve-copy-and-read-visio-shape-data_5.png)||
#### **阅读编程示例**
下面的代码片段读取形状数据（自定义属性）。


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReadAllShapeProps.class);  

// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");

for (Shape shape :(Iterable<Shape>) page.getShapes())
{
    if (shape.getName() == "Process1")
    {
        for (Prop property :(Iterable<Prop>) shape.getProps())
        {
            System.out.println(property.getLabel().getValue() + ": " + property.getValue().getVal());
        }
        break;
    }
}

{{< /highlight >}}


### **按名称读取形状属性**
下面的代码片段按名称（自定义属性）读取形状属性。
#### **按名称读取编程示例**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReadShapePropByName.class);   
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");

for (Shape shape :(Iterable<Shape>) page.getShapes())
{
    if (shape.getName() == "Process1")
    {
        Prop property = shape.getProps().getProp("Name1");
        System.out.println(property.getLabel().getValue() + ": " + property.getValue().getVal());
    }
}

{{< /highlight >}}


## **使用连接索引连接形状**
Aspose.Diagram for Java API 已经允许开发人员在形状上添加新的连接点，开发人员现在可以使用连接索引连接形状。
### **使用连接索引连接形状**
由公开的 ConnectShapesViaConnectorIndex 成员[页](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)类可用于使用连接索引连接形状。

1. 初始化一个新绘图。
1. 放置四个矩形
1. 添加两个额外的连接点，以便在底部边框线上有三个连接点
1. 使用动态连接器将每个底部连接的第一个形状连接到顶部的其他三个矩形形状
1. 保存图纸
#### **使用连接索引连接形状编程示例**
在您的 Java 应用程序中使用以下代码，使用连接索引与 Aspose.Diagram for Java API 连接形状。

## **检索子形状的父形状**
Aspose.Diagram for Java 允许开发人员检索子形状的父形状。
### **获取父形状**
这[形状](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape)类提供 ParentShape 属性来检索父形状。
#### **获取父形状编程示例**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveTheParentShape.class) + "Shapes\\";
		
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(13).getShapes().getShape(2);
Shape parentShape = shape.getParentShape();
System.out.println("Parent Shape's Properties:");
System.out.println("Shape ID: " + parentShape.getID());
System.out.println("Shape Name: " + parentShape.getName());
System.out.println("Shape Type: " + parentShape.getType());
{{< /highlight >}}


