+++
title = "Set Visio Shapes Line Data in Ruby" 
description = "" 
weight = 20133 
+++

Aspose.Diagram for Java : Set Visio Shape's Line Data in Ruby  

# Aspose.Diagram for Java : Set Visio Shape's Line Data in Ruby


## Aspose.Diagram - Set Visio Shape's Line Data

To Set Visio Shape's Line Data using **Aspose.Diagram Java for Ruby**, simply invoke **SetShapeLineData** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")shapes = diagram.getPages().getPage(0).getShapes()i = 0while i < shapes.getCount()    shape = shapes.get(i)    if shape.getNameU() == "rectangle" && shape.getID() == 1        shape.getLine().getLineColor().setValue(diagram.getPages().getPage(0).getShapes().getShape(1).getFill().getFillForegnd().getValue())        shape.getLine().getLineWeight().setValue(0.07041666666666667)        shape.getLine().getRounding().setValue(0.1)    end    i +=1end# Save diagramdiagram.save(data\_dir + "SetShapeLineData.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Set visio shape's line data."

## Download Running Code

Download **Set Visio Shape's Line Data (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapelinedata.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Shapes/setshapelinedata.rb)

