+++
title = "Get Shape Hyperlink Data from a Visio Drawing in Ruby" 
description = "" 
weight = 20155 
+++

Aspose.Diagram for Java : Get Shape Hyperlink Data from a Visio Drawing in Ruby  

# Aspose.Diagram for Java : Get Shape Hyperlink Data from a Visio Drawing in Ruby


## Aspose.Diagram - Get Shape Hyperlink Data

To Get Shape Hyperlink Data using **Aspose.Diagram Java for Ruby**, simply invoke **GetShapeHyperlinkData** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Hyperlinks.vdx")# Get a particular shapeshape = diagram.getPages().getPage("Flow 1").getShapes().getShape(1)hyperlinks = shape.getHyperlinks()i = 0while i < hyperlinks.getCount()    hyperlink = hyperlinks.get(i)    puts "Address: " + hyperlink.getAddress().getValue().to\_s    puts "Sub Address: " + hyperlink.getSubAddress().getValue().to\_s    puts "Description: " + hyperlink.getDescription().getValue().to\_s    i +=1end

## Download Running Code

Download **Get Shape Hyperlink Data from a Visio Drawing (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Hyperlinks/getshapehyperlinkdata.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Hyperlinks/getshapehyperlinkdata.rb)

