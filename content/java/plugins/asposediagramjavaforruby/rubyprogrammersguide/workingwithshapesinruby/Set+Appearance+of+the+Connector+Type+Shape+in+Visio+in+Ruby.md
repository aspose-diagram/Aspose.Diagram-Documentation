+++
title = "Set Appearance of the Connector Type Shape in Visio in Ruby" 
description = "" 
weight = 20129 
+++

Aspose.Diagram for Java : Set Appearance of the Connector Type Shape in Visio in Ruby  

# Aspose.Diagram for Java : Set Appearance of the Connector Type Shape in Visio in Ruby


## Aspose.Diagram - Set Appearance of the Connector Type Shape in Visio

To Set Appearance of the Connector Type Shape in Visio using **Aspose.Diagram Java for Ruby**, simply invoke **SetShapeAppearance** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")# Access a particular pagepage = diagram.getPages().getPage("Flow 1")# get a particular connector shapeshape = page.getShapes().getShape(1)# set dynamic connector appearanceshape.setConnectorsType(Rjb::import('com.aspose.diagram.ConnectorsTypeValue').STRAIGHT\_LINES)# Save diagramdiagram.save(data\_dir + "SetShapeAppearance.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Set appearnce of the connector type shape."

## Download Running Code

Download **Set Appearance of the Connector Type Shape in Visio (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapeappearance.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Shapes/setshapeappearance.rb)

