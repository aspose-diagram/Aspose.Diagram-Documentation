---
title: 检索 Visio 连接器和字体信息
type: docs
weight: 20
url: /zh/java/retrieve-visio-connectors-and-font-information/
---
## **检索连接器信息**
Aspose.Diagram for Java 提供检索信息的机制 - ID 和名称 - 关于[页数](/diagram/zh/java/retrieve-get-copy-and-insert-a-page/)和[掌握]().它还可以让您获得有关连接器（连接形状的元素）的信息。

这[连接](https://reference.aspose.com/diagram/java/com.aspose.diagram/connect)对象表示连接 Visio 绘图页上两个形状的连接器。 Connects 属性，由[页](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)类支持 Aspose.Diagram.Connect 对象的集合。此属性可用于检索有关连接器的 ID 和名称信息。

**显示以下代码输出的控制台窗口。** 

![待办事项：图片_替代_文本](retrieve-visio-connectors-and-font-information_1.png)
### **编程范例**
以下代码段检索 diagram 中连接器的信息。


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveConnectorInfo.class);
        
//Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "RetrieveConnectorInfo.vsd");        
for(Connect connector : (Iterable<Connect>) diagram.getPages().getPage(0).getConnects())
{
    // Display information about the Connectors
    System.out.println("\nFrom Shape ID : " + connector.getFromSheet());
    System.out.println("To Shape ID : " + connector.getToSheet());
 }

System.out.println("Process Completed Successfully");

{{< /highlight >}}

## **检索字体信息**
Aspose.Diagram 具有从中检索有关构成 diagram 的元素的信息的机制[页数](/diagram/zh/java/retrieve-get-copy-and-insert-a-page/), [模版](), [连接器](https://reference.aspose.com/diagram/java/com.aspose.diagram/ConnectCollection)还有字体。本文介绍如何找出 diagram 中使用了哪些字体。

这[字体](https://reference.aspose.com/diagram/java/com.aspose.diagram/font)对象表示应用于文档中的文本或可在系统上使用的字体。

字体对象将名称（例如“Arial”）映射到字体 ID（例如 3），字体 ID Microsoft Visio 存储在形状的字符部分的字体单元格中，该形状包含使用该字体设置格式的文本。当在不同系统上打开文档或安装或删除字体时，字体 ID 可能会发生变化。
### **检索字体编程示例**
下面这段代码从 Visio diagram 中检索字体信息。


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveFontInfo.class);

// call the diagram constructor to load diagram
Diagram diagram = new Diagram(dataDir+ "RetrieveFontInfo.vsd");

for(Font font : (Iterable<Font>) diagram.getFonts())
{
    // Display information about the fonts
    System.out.println(font.getName());
}

System.out.println("Process Completed Successfully");

{{< /highlight >}}


![待办事项：图片_替代_文本](retrieve-visio-connectors-and-font-information_2.png)
### **获取默认字体目录**
Aspose.Diagram for Java API 还允许使用 Diagram 类的 getDefaultFontDir() 方法获取默认字体目录路径。以下代码从 Visio diagram 中检索默认字体目录。


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveFontInfo.class) + "Diagrams/";

// Call the diagram constructor to load diagram
Diagram diagram = new Diagram(dataDir + "RetrieveFontInfo.vsd");

// Display font default directory
System.out.println(diagram.getDefaultFontDir());

{{< /highlight >}}

