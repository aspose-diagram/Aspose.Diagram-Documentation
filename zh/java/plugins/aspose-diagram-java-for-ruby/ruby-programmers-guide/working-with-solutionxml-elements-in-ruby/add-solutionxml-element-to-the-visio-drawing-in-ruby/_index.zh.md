---
title: 将 SolutionXML 元素添加到 Ruby 中的 Visio 绘图
type: docs
weight: 10
url: /zh/java/add-solutionxml-element-to-the-visio-drawing-in-ruby/
---
## **Aspose.Diagram - 将 SolutionXML 元素添加到 Visio 绘图**
使用以下方法将 SolutionXML 元素添加到 Visio 绘图**Aspose.Diagram Java 红宝石** 只需调用**添加解决方案 XmlElement**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# initialize SolutionXML object

solution_xml = Rjb::import('com.aspose.diagram.SolutionXML').new

\# set name

solution_xml.setName("Solution XML")

\# set xml value

solution_xml.setXmlValue("XML Value")

\# add SolutionXML element

diagram.getSolutionXMLs().add(solution_xml)

\# save Visio diagram

diagram.save(data_dir + "SolutionXmlElement.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Added SolutionXML Element to the Visio Drawing."

{{< /highlight >}}
## **下载运行代码**
下载**将 SolutionXML 元素添加到 Visio 绘图 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/SolutionXML/addsolutionxmlelement.rb)
