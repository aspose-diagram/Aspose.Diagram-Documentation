---
title : "Remove All Macros from the Visio Diagram in Ruby" 
description : "" 
weight : 20114 
toc : false
type: docs
url: /java/plugins/ruby/guide/diagrams/remove+all+macros+from+the+visio+diagram+in+ruby/
---

# Aspose.Diagram for Java : Remove All Macros from the Visio Diagram in Ruby


## Aspose.Diagram - Remove All Macros from the Visio Diagram

To Remove All Macros from the Visio Diagram using **Aspose.Diagram Java for Ruby**, simply invoke **RemoveAllMacrosFromDiagram** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")# remove all macrosdiagram.setVbProjectData(nil)# Save as VDXdiagram.save(data\_dir + "RemoveAllMacros.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Removed all macros from diagram successfully!"

## Download Running Code

Download **Remove All Macros from the Visio Diagram (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/removeallmacrosfromdiagram.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Diagrams/removeallmacrosfromdiagram.rb)

