---
title : "Read Visio Shape Data in Ruby" 
description : "" 
weight : 20124 
toc : false
type: docs
url: /java/plugins/ruby/guide/shapes/read+visio+shape+data+in+ruby/
---

# Aspose.Diagram for Java : Read Visio Shape Data in Ruby


## Aspose.Diagram - Read All Shape Properties

To Read All Shape Properties using **Aspose.Diagram Java for Ruby**, call **read\_all\_shape\_properties** method of **ReadShapeData** module. Here you can see example code.

**Ruby Code**

{{< code lang="cs" >}}
def read_all_shape_properties()
    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Create instance of Diagram
    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    shapes = diagram.getPages().getPage(0).getShapes()
    
    i = 0
    while i < shapes.getCount()
        shape = shapes.get(i)
        if shape.getName() == "Process"
            j = 0
            while j < shape.getProps().getCount()
                property = shape.getProps().get(j)
                puts property.getLabel().getValue() + ": " + property.getValue().getVal()
                j +=1
            end
            break
        end

        i +=1
    end
end
{{< /code >}}

## Aspose.Diagram - Read a Shape Property by Name

To Read a Shape Property by Name using **Aspose.Diagram Java for Ruby**, call **read\_shape\_property\_by\_name** method of **ReadShapeData** module. Here you can see example code.

**Ruby Code**

{{< code lang="cs" >}}
def read_shape_property_by_name()
    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Create instance of Diagram
    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    shapes = diagram.getPages().getPage(0).getShapes()
    
    i = 0
    while i < shapes.getCount()
        shape = shapes.get(i)
        if shape.getName() == "Process"
            property = shape.getProps().getProp("Cost")
            puts property.getLabel().getValue() + ": " + property.getValue().getVal()
        end
        i +=1
    end
end
{{< /code >}}

## Download Running Code

Download **Read Visio Shape Data (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/readshapedata.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Shapes/readshapedata.rb)

