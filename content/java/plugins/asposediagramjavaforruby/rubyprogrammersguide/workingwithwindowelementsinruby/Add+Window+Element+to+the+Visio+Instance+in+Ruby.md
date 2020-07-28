+++
title = "Add Window Element to the Visio Instance in Ruby" 
description = "" 
weight = 20141 
+++

Aspose.Diagram for Java : Add Window Element to the Visio Instance in Ruby  

# Aspose.Diagram for Java : Add Window Element to the Visio Instance in Ruby


## Aspose.Diagram - Add Window Element to the Visio Instance

To Add Window Element to the Visio Instance using **Aspose.Diagram Java for Ruby**, simply invoke **AddWindowElement** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")# initialize window objectwindow = Rjb::import('com.aspose.diagram.Window').new# set window statewindow.setWindowState(Rjb::import('com.aspose.diagram.WindowStateValue').MAXIMIZED)# set window heightwindow.setWindowHeight(500)# set window widthwindow.setWindowWidth(500)# set window typewindow.setWindowType(Rjb::import('com.aspose.diagram.WindowTypeValue').STENCIL)# add window objectdiagram.getWindows().add(window)# save in any supported formatdiagram.save(data\_dir + "AddWindowElement.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Added window element to the visio instance."

## Download Running Code

Download **Add Window Element to the Visio Instance (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/addwindowelement.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/WindowElements/addwindowelement.rb)

