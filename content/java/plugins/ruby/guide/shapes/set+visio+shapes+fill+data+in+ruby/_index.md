---
title : "Set Visio Shapes Fill data in Ruby" 
description : "" 
weight : 20132 
toc : false
type: docs
url: /java/plugins/ruby/guide/shapes/set+visio+shapes+fill+data+in+ruby/
---

# Aspose.Diagram for Java : Set Visio Shape's Fill data in Ruby


## Aspose.Diagram - Set Visio Shape's Fill data

To Set Visio Shape's Fill data using **Aspose.Diagram Java for Ruby**, simply invoke **SetShapeFillData** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")shapes = diagram.getPages().getPage(0).getShapes()i = 0while i < shapes.getCount()    shape = shapes.get(i)    if shape.getNameU() == "rectangle" && shape.getID() == 1        shape.getFill().getFillBkgnd().setValue(diagram.getPages().getPage(0).getShapes().getShape(0).getFill().getFillBkgnd().getValue())        shape.getFill().getFillForegnd().setValue("#ebf8df")    end    i +=1end# Save diagramdiagram.save(data\_dir + "SetShapeFillData.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Set visio shape's fill data."

## Download Running Code

Download **Set Visio Shape's Fill data (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapefilldata.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Shapes/setshapefilldata.rb)

