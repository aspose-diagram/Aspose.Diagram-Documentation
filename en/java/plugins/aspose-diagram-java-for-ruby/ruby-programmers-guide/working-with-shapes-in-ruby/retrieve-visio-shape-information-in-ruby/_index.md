---
title: Retrieve Visio Shape Information in Ruby
type: docs
weight: 70
url: /java/retrieve-visio-shape-information-in-ruby/
---

## **Aspose.Diagram - Retrieve Visio Shape Information**
To Retrieve Visio Shape Information using **Aspose.Diagram Java for Ruby**, simply invoke **GetShapeInfo** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

shapes = diagram.getPages().getPage(0).getShapes()

i = 0

while i < shapes.getCount()

    shape = shapes.get(i)

    # Display information about the shapes

    puts "Shape ID : " + shape.getID().to_s

    puts "Name : " + shape.getName().to_s

    puts "Master Shape : " + shape.getMaster().getName().to_s

    i +=1

end

{{< /highlight >}}
## **Download Running Code**
Download **Retrieve Visio Shape Information (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/getshapeinfo.rb)
