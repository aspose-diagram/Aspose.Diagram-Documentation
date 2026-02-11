---
title: 获取 Visio 形状包括儿童
type: docs
weight: 110
url: /zh/net/get-visio-shape-including-child/
description: 本节介绍如何获取 visio 形状，包括形状 ID 或名称为 Aspose.Diagram 的孩子。
---
### **检索包含子项的 Visio 形状**
diagram 中的每个形状都有一个 ID 和一个名称。使用 Visio 编程时 ID 很重要：它是访问形状的主要方法。每个形状还保留有关其制作母版（模板）的信息。

一个[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)是 Visio 绘图中的一个对象，可能有父亲或儿子。 Page 类公开的 Shapes 属性支持 Aspose.Diagram.Shape 对象的集合。 Shapes 属性可用于检索有关形状的信息。
#### **检索 Visio 形状编程示例**
以下代码片段检索包含子项的形状。请检查此示例代码：

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "NetworkConnection.vsdx");

Page page = diagram.Pages[0];

Shape shapeContainerChild = page.Shapes.GetShapeIncludingChild("RectangleChild");

if (shapeContainerChild == null)
    throw new Exception();
    
// Save visio diagram
diagram.Save(dataDir + "GroupShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

