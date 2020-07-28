+++
title = "Connect Sub-shapes of the Groups in Ruby" 
description = "" 
weight = 20121 
+++

Aspose.Diagram for Java : Connect Sub-shapes of the Groups in Ruby  

# Aspose.Diagram for Java : Connect Sub-shapes of the Groups in Ruby


## Aspose.Diagram - Connect Sub-shapes of the Groups

To Connect Sub-shapes of the Groups using **Aspose.Diagram Java for Ruby**, simply invoke **ConnectSubShapes** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")# Access a particular pagepage = diagram.getPages().getPage("Flow 1")# Set sub shape idsshape\_from\_id = 1shape\_to\_id = 9# Initialize connector shapeshape = Rjb::import('com.aspose.diagram.Shape').newshape.getLine().getEndArrow().setValue(5)shape.getLine().getLineWeight().setValue(0.01388)# Add shapeconnecter\_id = diagram.addShape(shape, "Dynamic connector", page.getID())# Connect sub-shapesconnection\_point\_place = Rjb::import('com.aspose.diagram.ConnectionPointPlace')page.connectShapesViaConnector(shape\_from\_id, connection\_point\_place.RIGHT, shape\_to\_id, connection\_point\_place.LEFT, connecter\_id)# Save diagramdiagram.save(data\_dir + "ConnectSubShapes.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Connected sub-shapes of a group."

## Download Running Code

Download **Connect Sub-shapes of the Groups (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/connectsubshapes.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Shapes/connectsubshapes.rb)

