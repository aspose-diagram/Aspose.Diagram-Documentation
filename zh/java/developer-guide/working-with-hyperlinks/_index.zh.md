---
title: 使用超链接
type: docs
weight: 110
url: /zh/java/working-with-hyperlinks/
---
## **将超链接添加到 Visio 形状**
这是一种动态添加超链接到 Microsoft Visio 形状的简单方法。

在多页 Visio 图纸上，超链接可以将您从一页移动到另一页。您还可以将绘图链接到网页或系统上的文件。

这些属性由[形状](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape)类支持[com.aspose.diagram.Hyperlink](https://reference.aspose.com/diagram/java/com.aspose.diagram/hyperlink)目的。 add 方法可用于添加形状的超链接数据。

识别 Microsoft Visio 中的属性：

1. 在 diagram 中，右键单击一个形状。
1. 选择**超级链接**.
1. 设置现有属性
1. 按**好的**按钮

**形状的超链接数据，如 Microsoft Visio 所示**

![待办事项：图片_替代_文本](working-with-hyperlinks_1.png)

下面的代码片段添加了形状的超链接数据。
### **添加超链接编程示例**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddHyperlinkToShape.class);   
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by ID
Shape shape = page.getShapes().getShape(2);

//initialize Hyperlink object
Hyperlink hyperlink = new Hyperlink();
//set address value
hyperlink.getAddress().setValue("http://www.google.com/");
//set sub address value
hyperlink.getSubAddress().setValue("Sub address here");
//set description value
hyperlink.getDescription().setValue("Description here");
//set name
hyperlink.setName("MyHyperLink");

//add hyperlink to the shape
shape.getHyperlinks().add(hyperlink);            
//save diagram to local space
diagram.save(dataDir + "AddHyperlinkToShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **获取 Visio 形状的超链接数据**
可以用与您类似的方式获取形状的超链接数据[读取 Visio 形状数据]().

开发人员可以使用与他们相同的方式从 Visio 形状中检索所有超链接[读取 Visio 形状数据]()使用[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/)

在多页 Visio 图纸中，超链接可以将您从一页移动到另一页。您还可以将绘图链接到网页或系统上的文件。

这些属性由[形状](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape)类支持[com.aspose.diagram.Hyperlink](https://reference.aspose.com/diagram/java/com.aspose.diagram/hyperlink)目的。该属性可用于读取形状的超链接数据。

识别 Microsoft Visio 中的属性：

1. 在 diagram 中，右键单击一个形状。
1. 选择**超链接。**
对话框中列出了任何现有属性。

**形状的超链接数据，如 Microsoft Visio 所示**

![待办事项：图片_替代_文本](working-with-hyperlinks_2.png)

**显示形状数据输出的控制台窗口**

![待办事项：图片_替代_文本](working-with-hyperlinks_3.png)

下面的代码片段读取形状的超链接数据。
### **获取超链接编程示例**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetHyperlinks.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by ID
Shape shape = page.getShapes().getShape(1);
// iterate through the hyperlinks
for (Hyperlink hyperlink :(Iterable<Hyperlink>) shape.getHyperlinks())
{
    System.out.println("Address: " + hyperlink.getAddress().getValue());
    System.out.println("Sub Address: " + hyperlink.getSubAddress().getValue());
    System.out.println("Description: " + hyperlink.getDescription().getValue());
}

{{< /highlight >}}

