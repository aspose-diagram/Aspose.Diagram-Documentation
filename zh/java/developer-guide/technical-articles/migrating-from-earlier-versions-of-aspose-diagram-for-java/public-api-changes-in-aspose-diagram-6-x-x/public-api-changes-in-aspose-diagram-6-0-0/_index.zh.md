---
title: 公共 API Aspose.Diagram 6.0.0 的变化
type: docs
weight: 50
url: /zh/java/public-api-changes-in-aspose-diagram-6-0-0/
---
{{% alert color="primary" %}} 

本文档描述了 Aspose.Diagram API 从版本 5.9.0 到 6.0.0 的更改，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对 Aspose.Diagram 中幕后行为的任何更改的描述。

{{% /alert %}} 
### **Shape 类中添加了 isGlued 方法**
isGlued 方法将一个形状对象作为参数来确定两个形状是否粘合。
示例代码：

**Java**

{{< highlight "java" >}}

 // Call the diagram constructor to load diagram

Diagram diagram = new Diagram("C:/temp/Drawing1.vsdx");

// get Visio page by name

Page page = diagram.getPages().getPage("Page-1");

// get Visio shapes by ids

Shape ShapedOne = page.getShapes().getShape(1);

Shape ShapedTwo = page.getShapes().getShape(2);

// determine whether shapes are glued

boolean glued = ShapedOne.isGlued(ShapedTwo);

{{< /highlight >}}
### **Shape 类中添加了 isConnected 方法**
isConnected 方法将一个形状对象作为参数来确定两个形状是否连接。
示例代码：

**Java**

{{< highlight "java" >}}

 // Call the diagram constructor to load diagram

Diagram diagram = new Diagram("C:/temp/Drawing1.vsdx");

// get Visio page by name

Page page = diagram.getPages().getPage("Page-1");

// get Visio shapes by ids

Shape ShapedOne = page.getShapes().getShape(1);

Shape ShapedTwo = page.getShapes().getShape(2);

// determine whether shapes are connected

boolean connected = ShapedOne.isConnected(ShapedTwo);

{{< /highlight >}}
