---
title: 在 Visio 页面中自动放置一组形状
type: docs
weight: 30
url: /zh/java/auto-space-a-collection-of-shapes-in-the-visio-page/
---
## **在 Visio 页面中自动放置一组形状**
使用 Aspose.Diagram for Java API，开发人员可以在 Visio 绘图中自动放置一组形状。为了实现这一点，Page 类提供了 autoSpaceShapes 成员，它采用 ShapeCollection 和 AutoSpaceOptions 参数。 AutoSpaceOptions 类允许设置水平和垂直距离。
### **页面中的自动空间形状**
在 Java 应用程序中使用以下代码在 Visio 绘图的任何页面中自动放置一组形状。

**Java**

{{< highlight "java" >}}

 // load a Visio drawing

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// get page of the Visio drawing

Page page = diagram.getPages().getPage("Page-1");

// initialize auto space options

AutoSpaceOptions options = new AutoSpaceOptions();

// set horizontal and vertical distances

options.setDistanceInHorizontal(2);

options.setDistanceInVertical(2);

// set auto space 

page.autoSpaceShapes(page.getShapes(), options);

// save Visio drawing

diagram.save("c:\\temp\\AutoSpaceShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
