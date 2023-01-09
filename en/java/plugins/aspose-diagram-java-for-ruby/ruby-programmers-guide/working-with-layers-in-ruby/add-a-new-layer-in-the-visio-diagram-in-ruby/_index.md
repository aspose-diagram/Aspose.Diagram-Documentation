---
title: Add a new Layer in the Visio Diagram in Ruby
type: docs
weight: 10
url: /java/add-a-new-layer-in-the-visio-diagram-in-ruby/
---

## **Aspose.Diagram - Add a new Layer**
To Add a new Layer using **Aspose.Diagram Java for Ruby**, simply invoke **AddNewLayer** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Basic_Shapes.vsd")

\# get Visio page

page = diagram.getPages().getPage(0)

\# initialize a new Layer class object

layer = Rjb::import('com.aspose.diagram.Layer').new

\# set Layer name

layer.getName().setValue("Layer2")

\# set Layer Visibility

layer.getVisible().setValue(2)

\# add Layer to the particular page sheet

page.getPageSheet().getLayers().add(layer)

\# add a new shape

shape_id = page.addShape(3.0, 3.0, 0.36, 0.36, "Circle")

\# get the Shape object

shape = page.getShapes().getShape(shape_id)

\# assign this new Layer

shape.getLayerMem().getLayerMember().setValue(layer.getIX().to_s)

\# Save diagram

diagram.save(data_dir + "AddNewLayer.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Added a new Layer in the Visio Diagram."

{{< /highlight >}}
## **Download Running Code**
Download **Add a new Layer in the Visio Diagram (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Layers/addnewlayer.rb)
