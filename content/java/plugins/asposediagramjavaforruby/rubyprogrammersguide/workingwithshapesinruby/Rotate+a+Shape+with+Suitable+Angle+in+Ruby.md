+++
title = "Rotate a Shape with Suitable Angle in Ruby" 
description = "" 
weight = 20127 
+++

Aspose.Diagram for Java : Rotate a Shape with Suitable Angle in Ruby  

# Aspose.Diagram for Java : Rotate a Shape with Suitable Angle in Ruby


## Aspose.Diagram - Rotate a Shape with Suitable Angle

To Rotate a Shape with Suitable Angle using **Aspose.Diagram Java for Ruby**, simply invoke **RotateShape** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")# Add a shape and set the anglediagram.getPages().getPage(0).getShapes().getShape(1).setAngle(190)# Save diagramdiagram.save(data\_dir + "RotateShape.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Rotated shape."

## Download Running Code

Download **Rotate a Shape with Suitable Angle (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/rotateshape.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Shapes/rotateshape.rb)

