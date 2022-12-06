---
title: 从 Ruby 中的 SolutionXML 元素读取 XML 值
type: docs
weight: 20
url: /zh/java/reading-xml-values-from-the-solutionxml-element-in-ruby/
---
## **Aspose.Diagram - 从 SolutionXML 元素读取 XML 值**
使用 SolutionXML 元素读取 XML 值**Aspose.Diagram Java 红宝石** 只需调用**读取 XmlValues**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

数据_dir = File.dirname(File.dirname(File.dirname(File.dirname(__文件__)))) + '/数据/'

\# 创建 Diagram 实例

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "SolutionXmlElement.vdx")

solution_xmls = diagram.getSolutionXMLs()

我 = 0

当我< solution_xmls.getCount()

    solution_xml = solution_xmls.get(i)

    # get name property

    puts "Name: " + solution_xml.getName().to_s

    # get xml value

    puts "Value:" + solution_xml.getXmlValue().to_s

    i +=1

end

{{< /highlight >}}
## **下载运行代码**
下载**从 SolutionXML 元素读取 XML 值 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/SolutionXML/readxmlvalues.rb)
