---
title: 合并组合 Diagram
type: docs
weight: 30
url: /zh/net/merge-combine-diagram/
description: 本节说明如何合并 visio 文件
---
## **可能的使用场景**

Aspose.Diagram 允许您将两个 visio 文件合并为一个。
 Aspose.Diagram for .NET API 有[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)表示 Visio 绘图的类。
使用方法[**结合**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/methods/combine)在[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)组合图表的类。

## **示例代码**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Load another Visio diagram
Diagram diagram2 = new Diagram(Drawing2.vsdx");
diagram2.Combine(diagram);

// Save the new Visio
newDiagram.Save(dataDir + "out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
