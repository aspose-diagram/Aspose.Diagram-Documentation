---
title: Добавьте элемент SolutionXML в чертеж Visio в Ruby
type: docs
weight: 10
url: /ru/java/add-solutionxml-element-to-the-visio-drawing-in-ruby/
---
## **Aspose.Diagram — добавление элемента SolutionXML в чертеж Visio**
 Чтобы добавить элемент SolutionXML в чертеж Visio с помощью**Aspose.Diagram Java для рубина** , просто вызовите**AddSolutionXmlElement** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

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
## **Скачать рабочий код**
 Скачать**Добавьте элемент SolutionXML в чертеж Visio (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/SolutionXML/addsolutionxmlelement.rb)
