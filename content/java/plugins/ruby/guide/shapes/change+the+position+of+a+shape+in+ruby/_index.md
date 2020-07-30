---
title : "Change the Position of a Shape in Ruby" 
description : "" 
weight : 20120 
toc : false
type: docs
url: /java/plugins/ruby/guide/shapes/change+the+position+of+a+shape+in+ruby/
---

# Aspose.Diagram for Java : Change the Position of a Shape in Ruby


## Aspose.Diagram - Change the Position of a Shape

To Change the Position of a Shape using **Aspose.Diagram Java for Ruby**, simply invoke **ChangeShapePosition** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")shapes = diagram.getPages().getPage(0).getShapes()i = 0while i < shapes.getCount()    shape = shapes.get(i)    if shape.getNameU() == "Process" && shape.getID() == 2        shape.move(1, 1)    end    i +=1end# Save diagramdiagram.save(data\_dir + "ChangeShapePosition.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Changed position of a shape."

## Download Running Code

Download **Change the Position of a Shape (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/changeshapeposition.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Shapes/changeshapeposition.rb)

