---
title: 获取 Visio 形状继承填充
type: docs
weight: 100
url: /zh/net/get-visio-shape-inherit-fill/
description: 本节介绍如何获取 visio 形状的填充样式，继承自其父样式并掌握 Aspose.Diagram。
---
### **检索 Visio 形状的继承填充数据**
Visio 形状可以继承父样式和主形状。开发者可以获得Visio形状的继承填充数据。 InheritFill 属性，由[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类，包含由父样式和主控形状继承的形状的填充格式值。
#### **检索继承的填充数据编程示例**
以下代码片段检索形状的继承填充数据。请检查此示例代码：

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
	Fill f = shape.InheritFill;
	Console.WriteLine(f.FillForegnd.Value);
	Console.WriteLine(f.FillPattern.Value);
	Console.WriteLine(f.ShdwForegnd.Value);
	Console.WriteLine(f.ShdwPattern.Value);
}

{{< /highlight >}}
```

