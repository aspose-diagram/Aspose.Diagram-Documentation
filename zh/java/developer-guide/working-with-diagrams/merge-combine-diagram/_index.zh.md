---
title: 合并组合 Diagram
type: docs
weight: 30
url: /zh/java/merge-combine-diagram/
description: 本节说明如何合并 visio 文件
---
## **可能的使用场景**

Aspose.Diagram 允许您将两个 visio 文件合并为一个。
 Aspose.Diagram for Java API 有[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram)表示 Visio 绘图的类。
使用方法[**结合**](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#combine(com.aspose.diagram.Diagram)） 在[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram)组合图表的类。

## **示例代码**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CombineDiagram.class);

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Load another Visio diagram
Diagram diagram2 = new Diagram(dataDir + Drawing2.vsdx");

diagram2.combine(diagram);

// save in the VSDX format
diagram.save(dataDir + "CombineDiagram_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

