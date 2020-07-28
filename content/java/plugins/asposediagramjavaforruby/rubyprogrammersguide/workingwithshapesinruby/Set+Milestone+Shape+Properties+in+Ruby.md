+++
title = "Set Milestone Shape Properties in Ruby" 
description = "" 
weight = 20130 
+++

Aspose.Diagram for Java : Set Milestone Shape Properties in Ruby  

# Aspose.Diagram for Java : Set Milestone Shape Properties in Ruby


## Aspose.Diagram - Set Milestone Shape Properties

To Set Milestone Shape Properties using **Aspose.Diagram Java for Ruby**, simply invoke **SetMilestoneShapeProperties** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")shape\_id = 1# Get timeline shapemilestone = diagram.getPages().getPage("Flow 1").getShapes().getShape(shape\_id)# Initialize MilestoneHelper objectmilestone\_helper = Rjb::import('com.aspose.diagram.MilestoneHelper').new(milestone)# Set date formatmilestone\_helper.setDateFormat(21)# Set auto update flagmilestone\_helper.setAutoUpdate(true)# Set milestone typemilestone\_helper.setType(6)# Save diagramdiagram.save(data\_dir + "SetMilestoneShapeProperties.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Set milestone shape properties."

## Download Running Code

Download **Set Milestone Shape Properties (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setmilestoneshapeproperties.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Shapes/setmilestoneshapeproperties.rb)

