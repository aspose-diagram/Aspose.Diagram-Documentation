---
title : "Configure Shape Objects with Layers in Visio in Ruby" 
description : "" 
weight : 20151 
toc : false
type: docs
url: /java/plugins/ruby/guide/layers/configure+shape+objects+with+layers+in+visio+in+ruby/
---

# Aspose.Diagram for Java : Configure Shape Objects with Layers in Visio in Ruby


## Aspose.Diagram - Configure Shape Objects with Layers

To Configure Shape Objects with Layers using **Aspose.Diagram Java for Ruby**, simply invoke **ConfigureShapeWithLayers** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")shapes = diagram.getPages().getPage("Flow 1").getShapes()i = 0while i < shapes.getCount()    shape = shapes.get(i)    #puts shape.getName().to\_s    if shape.getName() == "Process"        # Add shape1 in first two layers. Here "0;1" are indexes of the layers        layer = shape.getLayerMem()        layer.getLayerMember().setValue("0;1")    elsif shape.getName() == "Preparation"        # Remove shape2 from all the layers        layer = shape.getLayerMem()        layer.getLayerMember().setValue("")    end    i +=1end# Save diagramdiagram.save(data\_dir + "Layers.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Configured Shape Objects with Layers in Visio."

## Download Running Code

Download **Configure Shape Objects with Layers in Visio (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Layers/configureshapewithlayers.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Layers/configureshapewithlayers.rb)

