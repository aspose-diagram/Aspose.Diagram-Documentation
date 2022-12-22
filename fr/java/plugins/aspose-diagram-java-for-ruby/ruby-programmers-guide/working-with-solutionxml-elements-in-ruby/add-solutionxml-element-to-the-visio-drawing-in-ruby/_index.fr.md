---
title: Ajouter un élément SolutionXML au dessin Visio dans Ruby
type: docs
weight: 10
url: /fr/java/add-solutionxml-element-to-the-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Ajouter un élément SolutionXML au dessin Visio**
 Pour ajouter un élément SolutionXML au dessin Visio à l'aide de**Aspose.Diagram Java pour rubis** , invoquez simplement**AddSolutionXmlElementAddSolutionXmlElement** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

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
## **Télécharger le code d'exécution**
 Télécharger**Ajouter un élément SolutionXML au dessin Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/SolutionXML/addsolutionxmlelement.rb)
