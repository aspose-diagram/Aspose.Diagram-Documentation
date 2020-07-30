---
title : "Create an empty Visio Diagram in Ruby" 
description : "" 
weight : 20110 
toc : false
type: docs
url: /java/plugins/ruby/guide/diagrams/create+an+empty+visio+diagram+in+ruby/
---

# Aspose.Diagram for Java : Create an empty Visio Diagram in Ruby


## Aspose.Diagram - Create an empty Visio Diagram

To Create an empty Visio Diagram using **Aspose.Diagram Java for Ruby**, simply invoke **CreateDiagram** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new# Save as VDXdiagram.save(data\_dir + "CreateDiagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Created visio diagram successfully!"

## Download Running Code

Download **Create an empty Visio Diagram (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/creatediagram.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Diagrams/creatediagram.rb)

