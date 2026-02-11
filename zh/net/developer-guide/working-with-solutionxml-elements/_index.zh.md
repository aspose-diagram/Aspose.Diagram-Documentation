---
title: 使用 SolutionXML 元素
type: docs
weight: 110
url: /zh/net/working-with-solutionxml-elements/
description: 本节介绍如何添加 solutionXml 或从 Aspose.Diagram 的 solutionXml 元素获取 xml 值。
---
## **将 SolutionXML 元素添加到 Visio 绘图**
SolutionXML 是包含在 SolutionXML 元素中的格式良好的 XML，它提供了一种标准化的解决方案数据持久化方法。用户可以在文档级别存储 SolutionXML，它立即存储在 VisioDocument 元素中。通常，这是使用以下方法存储和检索 SolutionXML 的最简单方法[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

这[解决方案XML](http://www.aspose.com/api/net/diagram/aspose.diagram/solutionXML)类表示 Visio 图纸中的 SolutionXML 元素。 Add 方法，由[解决方案XML](http://www.aspose.com/api/net/diagram/aspose.diagram/solutionXML)类，允许添加 SolutionXML 元素。
### **添加 SolutionXML 元素编程示例**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_SolutionXML();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Initialize SolutionXML object
SolutionXML solXML = new SolutionXML();
// Set name
solXML.Name = "Solution XML";
// Set xml value
solXML.XmlValue = "XML Value";
// Add SolutionXML element
diagram.SolutionXMLs.Add(solXML);

// Save Visio diagram
diagram.Save(dataDir + "AddSolutionXMLElement_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **从 SolutionXML 元素读取 XML 值**
SolutionXML 是包含在 SolutionXML 元素中的格式良好的 XML，它提供了一种标准化的解决方案数据持久化方法。用户可以使用 SolutionXML 元素读取 XML 值[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

SolutionXMLs 属性，由[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)类，支持 Aspose.Diagram.SolutionXML 对象的集合。此属性可用于从 SolutionXML 元素读取 XML 值。
### **阅读 SolutionXML 元素编程示例**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_SolutionXML();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Iterate through SolutionXML elements
foreach (SolutionXML solutionXML in diagram.SolutionXMLs)
{
    // Get name property
    Console.WriteLine(solutionXML.Name);
    // Get xml value
    Console.WriteLine(solutionXML.XmlValue);
}

{{< /highlight >}}
```
