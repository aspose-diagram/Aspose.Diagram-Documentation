---
title : "Retrieve All Layers from the Visio Diagram in Ruby" 
description : "" 
weight : 20152 
toc : false
type: docs
url: /java/plugins/ruby/guide/layers/retrieve+all+layers+from+the+visio+diagram+in+ruby/
---

# Aspose.Diagram for Java : Retrieve All Layers from the Visio Diagram in Ruby


## Aspose.Diagram - Retrieve All Layers

To Retrieve All Layers using **Aspose.Diagram Java for Ruby**, simply invoke **GetAllLayers** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")# get Visio pagepage = diagram.getPages().getPage(0)layers = page.getPageSheet().getLayers()i = 0while i < layers.getCount()    layer = layers.get(i)    puts "Name: " + layer.getName().getValue().to\_s    puts "Visibility: " + layer.getVisible().getValue().to\_s    puts "Status: " + layer.getStatus().getValue().to\_s        i +=1end

## Download Running Code

Download **Retrieve All Layers from the Visio Diagram (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Layers/getalllayers.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Layers/getalllayers.rb)

