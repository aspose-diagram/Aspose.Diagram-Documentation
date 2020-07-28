+++
title = "Add Support of Dynamic Grids and Connection Points in Ruby" 
description = "" 
weight = 20140 
+++

Aspose.Diagram for Java : Add Support of Dynamic Grids and Connection Points in Ruby  

# Aspose.Diagram for Java : Add Support of Dynamic Grids and Connection Points in Ruby


## Aspose.Diagram - Add Support of Dynamic Grids and Connection Points

To Add Support of Dynamic Grids and Connection Points using **Aspose.Diagram Java for Ruby**, simply invoke **AddDynamicGridsAndConnectionPoints** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")# get window object by indexwindow = diagram.getWindows().get(0)# check dynamic grid optionwindow.setDynamicGridEnabled(1)# check connection points optionwindow.setShowConnectionPoints(1)# Save as VDXdiagram.save(data\_dir + "AddDynamicGridsAndConnectionPoints.vsx", Rjb::import('com.aspose.diagram.SaveFileFormat').VSX)puts "Added Support of Dynamic Grids and Connection Points in the Visio Drawings."

## Download Running Code

Download **Add Support of Dynamic Grids and Connection Points (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/adddynamicgridsandconnectionpoints.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/WindowElements/adddynamicgridsandconnectionpoints.rb)

