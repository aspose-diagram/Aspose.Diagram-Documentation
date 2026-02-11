---
title: 获取 Visio 形状继承字符
type: docs
weight: 101
url: /zh/net/get-visio-shape-inherit-chars/
description: 本节介绍如何获取 visio 形状的字体样式从其父样式继承并掌握 Aspose.Diagram。
---
### **检索 Visio 形状的继承字体数据**
 Visio 形状可以继承父样式和主形状。开发者可以获取或设置一个Visio形状的继承字体数据。 InheritLine 属性，由[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类，包含由父样式和主控形状继承的形状的线条格式值。
#### **检索继承的字体数据编程示例**
以下代码片段检索形状的继承字体数据。请检查此示例代码：

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
	Aspose.Diagram.Char ch = shape.InheritChars.GetChar(0);
	Console.WriteLine(ch.Style.Value);
	Console.WriteLine(ch.Color.Value); 
	Console.WriteLine(ch.FontName.Value); 
	Console.WriteLine(ch.Size.Value);
	Console.WriteLine(ch.Case.Value);
	Console.WriteLine(ch.IsUnderline);
	Console.WriteLine(ch.IsItalic);
	Console.WriteLine(ch.IsStrikethrough);
	Console.WriteLine(ch.IsDoubleStrikethrough);
	Console.WriteLine(ch.IsSubscript);
	Console.WriteLine(ch.IsSuperscript); 
}

{{< /highlight >}}
```

