---
title : "Protect and Unprotect Diagrams in Ruby" 
description : "" 
weight : 20162 
toc : false
type: docs
url: /java/plugins/ruby/guide/protection/protect+and+unprotect+diagrams+in+ruby/
---

# Aspose.Diagram for Java : Protect and Unprotect Diagrams in Ruby


## Aspose.Diagram - Protect and Unprotect Diagrams

To Protect and Unprotect Diagrams using **Aspose.Diagram Java for Ruby**, simply invoke **ProtectUnprotectDiagram** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")diagram.getDocumentSettings().setProtectBkgnds(1)diagram.getDocumentSettings().setProtectMasters(1)diagram.getDocumentSettings().setProtectShapes(1)diagram.getDocumentSettings().setProtectStyles(1)# Save diagramdiagram.save(data\_dir + "ProtectUnprotectDiagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Applied protection on diagram successfully!"

## Download Running Code

Download **Protect and Unprotect Diagrams (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Protection/protectunprotectdiagram.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Protection/protectunprotectdiagram.rb)

