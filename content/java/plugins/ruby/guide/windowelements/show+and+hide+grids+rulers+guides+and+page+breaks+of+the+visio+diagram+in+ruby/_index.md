---
title : "Show and Hide Grids Rulers Guides and Page Breaks of the Visio Diagram in Ruby" 
description : "" 
weight : 20143 
toc : false
type: docs
url: /java/plugins/ruby/guide/windowelements/show+and+hide+grids+rulers+guides+and+page+breaks+of+the+visio+diagram+in+ruby/
---

# Aspose.Diagram for Java : Show and Hide Grids, Rulers, Guides and Page Breaks of the Visio Diagram in Ruby


## Aspose.Diagram - Show and Hide Grids, Rulers, Guides and Page Breaks of the Visio Diagram

To Show and Hide Grids, Rulers, Guides and Page Breaks of the Visio Diagram using **Aspose.Diagram Java for Ruby**, simply invoke **ShowHideProperties** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")# get window object by indexwindow = diagram.getWindows().get(0)# set visibility of gridwindow.setShowGrid(1)# set visibility of guideswindow.setShowGuides(1)# set visibility of rulerswindow.setShowRulers(1)# set visibility of page breakswindow.setShowPageBreaks(1)# save in any supported formatdiagram.save(data\_dir + "ShowHideProperties.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Show and Hide Grids, Rulers, Guides and Page Breaks of the Visio Diagram."

## Download Running Code

Download **Show and Hide Grids, Rulers, Guides and Page Breaks of the Visio Diagram (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/showhideproperties.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/WindowElements/showhideproperties.rb)

