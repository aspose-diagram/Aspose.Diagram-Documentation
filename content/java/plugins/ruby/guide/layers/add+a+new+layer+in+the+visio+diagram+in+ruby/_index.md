---
title : "Add a new Layer in the Visio Diagram in Ruby" 
description : "" 
weight : 20150 
toc : false
type: docs
url: /java/plugins/ruby/guide/layers/add+a+new+layer+in+the+visio+diagram+in+ruby/
---

# Aspose.Diagram for Java : Add a new Layer in the Visio Diagram in Ruby


## Aspose.Diagram - Add a new Layer

To Add a new Layer using **Aspose.Diagram Java for Ruby**, simply invoke **AddNewLayer** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Basic\_Shapes.vsd")# get Visio pagepage = diagram.getPages().getPage(0)# initialize a new Layer class objectlayer = Rjb::import('com.aspose.diagram.Layer').new# set Layer namelayer.getName().setValue("Layer2")# set Layer Visibilitylayer.getVisible().setValue(2)# add Layer to the particular page sheetpage.getPageSheet().getLayers().add(layer)# add a new shapeshape\_id = page.addShape(3.0, 3.0, 0.36, 0.36, "Circle")# get the Shape objectshape = page.getShapes().getShape(shape\_id)# assign this new Layershape.getLayerMem().getLayerMember().setValue(layer.getIX().to\_s)# Save diagramdiagram.save(data\_dir + "AddNewLayer.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Added a new Layer in the Visio Diagram."

## Download Running Code

Download **Add a new Layer in the Visio Diagram (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Layers/addnewlayer.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Layers/addnewlayer.rb)

