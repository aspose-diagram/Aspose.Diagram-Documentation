---
title : "Set the Height and Width of a Shape in Ruby" 
description : "" 
weight : 20131 
toc : false
type: docs
url: /java/plugins/ruby/guide/shapes/set+the+height+and+width+of+a+shape+in+ruby/
---

# Aspose.Diagram for Java : Set the Height and Width of a Shape in Ruby


## Aspose.Diagram - Set the Height and Width of a Shape

To Set the Height and Width of a Shape using **Aspose.Diagram Java for Ruby**, simply invoke **SetShapeHeightAndWidth** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")shapes = diagram.getPages().getPage(0).getShapes()i = 0while i < shapes.getCount()    shape = shapes.get(i)    if shape.getNameU() == "Process" && shape.getID() == 1        shape.setWidth(2 \* shape.getXForm().getWidth().getValue())        shape.setHeight(2 \* shape.getXForm().getHeight().getValue())    end    i +=1end# Save diagramdiagram.save(data\_dir + "SetShapeHeightAndWidth.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Set height and width of shape."

## Download Running Code

Download **Set the Height and Width of a Shape (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapeheightandwidth.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Shapes/setshapeheightandwidth.rb)

