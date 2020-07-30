---
title : "Add SolutionXML Element to the Visio Drawing in Ruby" 
description : "" 
weight : 20145 
toc : false
type: docs
url: /java/plugins/ruby/guide/solutionxmlelements/add+solutionxml+element+to+the+visio+drawing+in+ruby/
---

# Aspose.Diagram for Java : Add SolutionXML Element to the Visio Drawing in Ruby


## Aspose.Diagram - Add SolutionXML Element to the Visio Drawing

To Add SolutionXML Element to the Visio Drawing using **Aspose.Diagram Java for Ruby**, simply invoke **AddSolutionXmlElement** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")# initialize SolutionXML objectsolution\_xml = Rjb::import('com.aspose.diagram.SolutionXML').new# set namesolution\_xml.setName("Solution XML")# set xml valuesolution\_xml.setXmlValue("XML Value")# add SolutionXML elementdiagram.getSolutionXMLs().add(solution\_xml)# save Visio diagramdiagram.save(data\_dir + "SolutionXmlElement.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Added SolutionXML Element to the Visio Drawing."

## Download Running Code

Download **Add SolutionXML Element to the Visio Drawing (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/SolutionXML/addsolutionxmlelement.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/SolutionXML/addsolutionxmlelement.rb)

