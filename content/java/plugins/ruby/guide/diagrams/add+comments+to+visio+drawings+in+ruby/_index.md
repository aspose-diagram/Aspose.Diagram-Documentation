---
title : "Add Comments to Visio Drawings in Ruby" 
description : "" 
weight : 20113 
toc : false
type: docs
url: /java/plugins/ruby/guide/diagrams/add+comments+to+visio+drawings+in+ruby/
---

# Aspose.Diagram for Java : Add Comments to Visio Drawings in Ruby


## Aspose.Diagram - Add Comments to Visio Drawings

To Add Comments to Visio Drawings using **Aspose.Diagram Java for Ruby**, simply invoke **AddCommentToDiagram** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")# Add commentdiagram.getPages().getPage(0).addComment(7.205905511811023, 3.880708661417323, "test@")# Save as VDXdiagram.save(data\_dir + "AddComment.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Added comment successfully!"

## Download Running Code

Download **Add Comments to Visio Drawings (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/addcommenttodiagram.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Diagrams/addcommenttodiagram.rb)

