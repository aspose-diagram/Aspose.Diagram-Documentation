---
title: 从 PHP 中的 SolutionXML 元素读取 XML 值
type: docs
weight: 20
url: /zh/java/reading-xml-values-from-the-solutionxml-element-in-php/
---
## **Aspose.Diagram - 从 SolutionXML 元素读取 XML 值**
使用 SolutionXML 元素读取 XML 值**Aspose.Diagram Java 用于 PHP** 只需调用**读取 XmlValues**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vdx");

$solution_xmls=$diagram->getSolutionXMLs();

$i= 0;

while ($i<(int)(string)$solution_xmls->getCount()) {

$solution_xml =$solution_xmls->get($i);

\# get name property

print "Name: ".(string)$solution_xml->getName();

\# get xml value

print "Value:".(string)$solution_xml->getXmlValue();

$i += 1;

}

{{< /highlight >}}
## **下载运行代码**
下载**从 SolutionXML 元素读取 XML 值 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithSolutionXMLElements/ReadXmlValues.php)
