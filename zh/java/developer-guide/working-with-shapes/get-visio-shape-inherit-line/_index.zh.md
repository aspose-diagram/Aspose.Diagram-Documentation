---
title: 获取 Visio 形状继承线
type: docs
weight: 100
url: /zh/java/get-visio-shape-inherit-line/
description: 本节介绍如何获取 visio 形状的线条样式，继承自其父样式并掌握 Aspose.Diagram。
---
### **检索 Visio 形状的继承线数据**
Visio 形状可以继承父样式和主形状。开发者可以获取或设置一个Visio形状的继承线数据。 InheritLine 属性，由[形状](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)类，包含由父样式和主控形状继承的形状的线条格式值。
#### **检索继承的行数据编程示例**
以下代码片段检索形状的继承线数据。请检查此示例代码：

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveInheritedLine.class) + "Shapes/";

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.getPages().getPage("Page-1");
// Get shape by ID
Shape shape = page.getShapes().getShape(1);
//Get Inherit Line from the parent style and master
Line line = shape.getInheritLine();
// Get the line formatting values
System.out.println(line.getBeginArrow().getValue());
System.out.println(line.getBeginArrowSize().getValue());
System.out.println(line.getEndArrow().getValue());
System.out.println(line.getEndArrowSize().getValue());
System.out.println(line.getLineColor().getValue());
System.out.println(line.getLinePattern().getValue());
System.out.println(line.getLineWeight().getValue());
System.out.println(line.getRounding().getValue());

{{< /highlight >}}
```

