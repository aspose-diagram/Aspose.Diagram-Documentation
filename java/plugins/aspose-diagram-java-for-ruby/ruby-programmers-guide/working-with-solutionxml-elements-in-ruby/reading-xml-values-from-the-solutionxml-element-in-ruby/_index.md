---
title: Reading XML Values from the SolutionXML Element in Ruby
type: docs
weight: 20
url: /java/reading-xml-values-from-the-solutionxml-element-in-ruby/
---

## **Aspose.Diagram - Reading XML Values from the SolutionXML Element**
To Reading XML Values from the SolutionXML Element using **Aspose.Diagram Java for Ruby**, simply invoke **ReadXmlValues** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "SolutionXmlElement.vdx")

solution_xmls = diagram.getSolutionXMLs()

i = 0

while i < solution_xmls.getCount()

    solution_xml = solution_xmls.get(i)

    # get name property

    puts "Name: " + solution_xml.getName().to_s

    # get xml value

    puts "Value:" + solution_xml.getXmlValue().to_s

    i +=1

end

{{< /highlight >}}
## **Download Running Code**
Download **Reading XML Values from the SolutionXML Element (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/SolutionXML/readxmlvalues.rb)
- [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/SolutionXML/readxmlvalues.rb)
