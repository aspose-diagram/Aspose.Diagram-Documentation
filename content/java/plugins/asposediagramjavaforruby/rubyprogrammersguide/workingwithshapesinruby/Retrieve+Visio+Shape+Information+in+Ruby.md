+++
title = "Retrieve Visio Shape Information in Ruby" 
description = "" 
weight = 20126 
+++

Aspose.Diagram for Java : Retrieve Visio Shape Information in Ruby  

# Aspose.Diagram for Java : Retrieve Visio Shape Information in Ruby


## Aspose.Diagram - Retrieve Visio Shape Information

To Retrieve Visio Shape Information using **Aspose.Diagram Java for Ruby**, simply invoke **GetShapeInfo** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")shapes = diagram.getPages().getPage(0).getShapes()i = 0while i < shapes.getCount()    shape = shapes.get(i)    # Display information about the shapes    puts "Shape ID : " + shape.getID().to\_s    puts "Name : " + shape.getName().to\_s    puts "Master Shape : " + shape.getMaster().getName().to\_s    i +=1end

## Download Running Code

Download **Retrieve Visio Shape Information (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/getshapeinfo.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Shapes/getshapeinfo.rb)

