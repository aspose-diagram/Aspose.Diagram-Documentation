---
title: Agregue el elemento SolutionXML al dibujo Visio en Ruby
type: docs
weight: 10
url: /es/java/add-solutionxml-element-to-the-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Agregar elemento SolutionXML al dibujo Visio**
 Para agregar el elemento SolutionXML al dibujo Visio usando**Aspose.Diagram Java para rubí** , simplemente invocar**AddSolutionXmlElementAddSolutionXmlElement** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

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
## **Descargar código de ejecución**
 Descargar**Agregue el elemento SolutionXML al dibujo Visio (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/SolutionXML/addsolutionxmlelement.rb)
