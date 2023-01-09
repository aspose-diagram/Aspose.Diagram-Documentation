---
title: 将 SolutionXML 元素添加到 Visio PHP 绘图中
type: docs
weight: 10
url: /zh/java/add-solutionxml-element-to-the-visio-drawing-in-php/
---
## **Aspose.Diagram - 将 SolutionXML 元素添加到 Visio 绘图**
使用以下方法将 SolutionXML 元素添加到 Visio 绘图**Aspose.Diagram Java 用于 PHP** 只需调用**添加解决方案 XmlElement**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."drawing.vsd");

\# initialize SolutionXML object

$solution_xml=new SolutionXML();

\# set name

$solution_xml->setName("Solution XML");

\# set xml value

$solution_xml->setXmlValue("XML Value");

\# add SolutionXML element

$diagram->getSolutionXMLs()->add($solution_xml);

\# save Visio diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SolutionXmlElement.vdx", $saveFileFormat->VDX);

print "Added SolutionXML Element to the Visio Drawing.".PHP_EOL;

{{< /highlight >}}
## **下载运行代码**
下载**将 SolutionXML 元素添加到 Visio 绘图 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithSolutionXMLElements/AddSolutionXmlElement.php)
