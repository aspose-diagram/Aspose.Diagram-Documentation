---
title : "Set Visio Shapes XForm Data in Ruby" 
description : "" 
weight : 20134 
toc : false
type: docs
url: /java/plugins/ruby/guide/shapes/set+visio+shapes+xform+data+in+ruby/
---

# Aspose.Diagram for Java : Set Visio Shape's XForm Data in Ruby


## Aspose.Diagram - Set Visio Shape's XForm Data

To Set Visio Shape's XForm Data using **Aspose.Diagram Java for Ruby**, simply invoke **SetShapeXFormData** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")shapes = diagram.getPages().getPage(0).getShapes()i = 0while i < shapes.getCount()    shape = shapes.get(i)    if shape.getNameU() == "process" && shape.getID() == 1        shape.getXForm().getPinX().setValue(5)        shape.getXForm().getPinY().setValue(5)    end    i +=1end# Save diagramdiagram.save(data\_dir + "SetShapeXFormData.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Set visio shape's XForm data."

## Download Running Code

Download **Set Visio Shape's XForm Data (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapexformdata.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Shapes/setshapexformdata.rb)

