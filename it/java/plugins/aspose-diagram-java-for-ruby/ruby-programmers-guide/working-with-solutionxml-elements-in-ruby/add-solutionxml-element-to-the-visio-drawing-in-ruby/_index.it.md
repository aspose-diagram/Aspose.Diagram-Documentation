---
title: Aggiungere l'elemento SolutionXML al disegno Visio in Ruby
type: docs
weight: 10
url: /it/java/add-solutionxml-element-to-the-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Aggiunta dell'elemento SolutionXML al disegno Visio**
 Per aggiungere un elemento SolutionXML al disegno Visio utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**AddSolutionXmlElement** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

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
## **Scarica il codice in esecuzione**
 Scarica**Aggiunta dell'elemento SolutionXML al disegno Visio (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/SolutionXML/addsolutionxmlelement.rb)
