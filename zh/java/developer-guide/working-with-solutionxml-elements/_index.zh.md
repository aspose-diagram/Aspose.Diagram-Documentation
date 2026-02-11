---
title: 使用 SolutionXML 元素
type: docs
weight: 140
url: /zh/java/working-with-solutionxml-elements/
---
## **将 SolutionXML 元素添加到 Visio 绘图**
SolutionXML 是包含在 SolutionXML 元素中的格式良好的 XML，它提供了一种标准化的解决方案数据持久化方法。用户可以在文档级别存储 SolutionXML，它立即存储在 VisioDocument 元素中。通常，这是使用以下方法存储和检索 SolutionXML 的最简单方法[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).

这[解决方案XML](https://reference.aspose.com/diagram/java/com.aspose.diagram/SolutionXML)类表示 Visio 图纸中的 SolutionXML 元素。 Add 方法，由[解决方案XML](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/SolutionXML)类，允许添加 SolutionXML 元素。
### **添加 SolutionXML 元素编程示例**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddSolutionXMLElement.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// initialize SolutionXML object
SolutionXML solXML = new SolutionXML();
// set name
solXML.setName("Solution XML");
// set xml value
solXML.setXmlValue("XML Value");
// add SolutionXML element
diagram.getSolutionXMLs().add(solXML);

// save Visio diagram
diagram.save(dataDir + "AddSolutionXMLElement_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **从 SolutionXML 元素读取 XML 值**
SolutionXML 是包含在 SolutionXML 元素中的格式良好的 XML，它提供了一种标准化的解决方案数据持久化方法。用户可以使用 SolutionXML 元素读取 XML 值[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).

SolutionXMLs 属性，由[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram)类，支持 Aspose.Diagram.SolutionXML 对象的集合。此属性可用于从 SolutionXML 元素读取 XML 值。
### **阅读 SolutionXML 元素编程示例**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReadSolutionXMLElement.class);   
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// iterate through SolutionXML elements
for (SolutionXML solutionXML :(Iterable<SolutionXML>) diagram.getSolutionXMLs())
{
    // get name property
    System.out.println(solutionXML.getName());
    // get xml value
    System.out.println(solutionXML.getXmlValue());
}

{{< /highlight >}}
```
