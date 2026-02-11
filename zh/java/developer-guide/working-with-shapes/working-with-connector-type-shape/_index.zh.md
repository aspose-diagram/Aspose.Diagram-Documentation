---
title: 使用连接器类型形状
type: docs
weight: 80
url: /zh/java/working-with-connector-type-shape/
---
## **在 Visio 中设置连接器类型形状的外观**
本主题详细说明开发人员如何使用 Aspose.Diagram for Java 更改动态连接器类型形状的外观。
### **设置连接器外观**
公开的 SetConnectorsType 方法[形状](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)类可用于设置连接器类型形状的外观。

下面的代码显示了如何：

1. 加载示例 diagram。
1. 获取特定页面。
1. 获得特定的连接器形状。
1. 设置形状的外观。
1. 保存 diagram
#### **设置连接器外观编程样例**
在您的 Java 应用程序中使用以下代码，使用 Aspose.Diagram for Java 设置连接器类型形状的外观。

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetConnectorAppearance.class);  
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//get a particular page
Page page = diagram.getPages().getPage("Page-3");
//get a dynamic connector type shape by id
Shape shape = page.getShapes().getShape(18);
// set dynamic connector appearance
shape.setConnectorsType(ConnectorsTypeValue.STRAIGHT_LINES);

//saving Visio diagram
diagram.save(dataDir + "SetConnectorAppearance_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **选择连接器形状的重新布线选项**
ConFixedCode 属性由[布局](https://reference.aspose.com/diagram/java/com.aspose.diagram/layout)类可用于选择重新路由选项。 Layout 属性，由[形状](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape)类，会用到。

|<p>**如何选择重新路由选项** </p><p>![待办事项：图片_替代_文本](http://i.imgur.com/1O70sSA.png)</p>|
|:- |
下面的代码显示了如何：

1. 加载示例文件。
1. 获取特定页面。
1. 获得特定的连接器形状。
1. 设置重新路由选项。
1. 保存 diagram。
### **选择重新路由选项编程示例**
在您的 Java 应用程序中使用以下代码选择使用 Aspose.Diagram for Java 的连接器形状的重新布线选项。

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RerouteConnectors.class);   
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");

// get a particular connector shape
Shape shape = page.getShapes().getShape(18);
// set reroute option
shape.getLayout().getConFixedCode().setValue(ConFixedCodeValue.NEVER_REROUTE);

// save Visio diagram
diagram.save(dataDir + "RerouteConnectors_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
