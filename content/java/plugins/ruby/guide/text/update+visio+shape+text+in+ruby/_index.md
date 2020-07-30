---
title : "Update Visio Shape Text in Ruby" 
description : "" 
weight : 20138 
toc : false
type: docs
url: /java/plugins/ruby/guide/text/update+visio+shape+text+in+ruby/
---

# Aspose.Diagram for Java : Update Visio Shape Text in Ruby


## Aspose.Diagram - Update Visio Shape Text

To Update Visio Shape Text using **Aspose.Diagram Java for Ruby**, simply invoke **UpdateShapeText** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")shapes = diagram.getPages().getPage(0).getShapes()i = 0while i < shapes.getCount()    shape = shapes.get(i)    if shape.getNameU() == "Process" && shape.getID() == 1        shape.getText().getValue().clear()        shape.getText().getValue().add(Rjb::import('com.aspose.diagram.Txt').new("New Text"))    end    i +=1end# Save diagramdiagram.save(data\_dir + "UpdateShapeText.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Updated shape text."

## Download Running Code

Download **Update Visio Shape Text (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Text/updateshapetext.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Text/updateshapetext.rb)

