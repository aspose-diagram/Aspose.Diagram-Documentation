---
title: Fügen Sie das SolutionXML-Element zur Zeichnung Visio in Ruby hinzu
type: docs
weight: 10
url: /de/java/add-solutionxml-element-to-the-visio-drawing-in-ruby/
---
## **Aspose.Diagram – SolutionXML-Element zur Zeichnung Visio hinzugefügt**
 Um das SolutionXML-Element zur Visio-Zeichnung hinzuzufügen, verwenden Sie**Aspose.Diagram Java für Rubin** , einfach aufrufen**AddSolutionXmlElement** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

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
## **Laufcode herunterladen**
 Download**SolutionXML-Element zur Zeichnung Visio hinzufügen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/SolutionXML/addsolutionxmlelement.rb)
