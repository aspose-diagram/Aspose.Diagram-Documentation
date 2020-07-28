+++
title = "Select Reroute Option of the Connector Shape in Ruby" 
description = "" 
weight = 20128 
+++

Aspose.Diagram for Java : Select Reroute Option of the Connector Shape in Ruby  

# Aspose.Diagram for Java : Select Reroute Option of the Connector Shape in Ruby


## Aspose.Diagram - Select Reroute Option of the Connector Shape

To Select Reroute Option of the Connector Shape using **Aspose.Diagram Java for Ruby**, simply invoke **SelectRerouteOption** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")# Access a particular pagepage = diagram.getPages().getPage("Flow 1")# get a particular connector shapeshape = page.getShapes().getShape(1)# set reroute optionshape.getLayout().getConFixedCode().setValue(Rjb::import('com.aspose.diagram.ConFixedCodeValue').NEVER\_REROUTE)# Save diagramdiagram.save(data\_dir + "SelectRerouteOption.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Seleted reroute option of the connector shape."

## Download Running Code

Download **Select Reroute Option of the Connector Shape (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/selectrerouteoption.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Shapes/selectrerouteoption.rb)

