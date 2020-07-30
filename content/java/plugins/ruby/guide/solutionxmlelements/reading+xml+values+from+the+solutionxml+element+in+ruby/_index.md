---
title : "Reading XML Values from the SolutionXML Element in Ruby" 
description : "" 
weight : 20146 
toc : false
type: docs
url: /java/plugins/ruby/guide/solutionxmlelements/reading+xml+values+from+the+solutionxml+element+in+ruby/
---

# Aspose.Diagram for Java : Reading XML Values from the SolutionXML Element in Ruby


## Aspose.Diagram - Reading XML Values from the SolutionXML Element

To Reading XML Values from the SolutionXML Element using **Aspose.Diagram Java for Ruby**, simply invoke **ReadXmlValues** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "SolutionXmlElement.vdx")solution\_xmls = diagram.getSolutionXMLs()i = 0while i < solution\_xmls.getCount()    solution\_xml = solution\_xmls.get(i)    # get name property    puts "Name: " + solution\_xml.getName().to\_s    # get xml value    puts "Value:" + solution\_xml.getXmlValue().to\_s    i +=1end

## Download Running Code

Download **Reading XML Values from the SolutionXML Element (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/SolutionXML/readxmlvalues.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/SolutionXML/readxmlvalues.rb)

