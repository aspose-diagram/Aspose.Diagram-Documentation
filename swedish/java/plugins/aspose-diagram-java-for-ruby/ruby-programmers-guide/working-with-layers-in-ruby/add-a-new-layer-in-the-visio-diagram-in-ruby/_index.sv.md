---
title: Lägg till ett nytt lager i Visio Diagram i Ruby
type: docs
weight: 10
url: /sv/java/add-a-new-layer-in-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Lägg till ett nytt lager**
 För att lägga till ett nytt lager med**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**Lägg till nytt lager** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

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
## **Ladda ner Running Code**
 Ladda ner**Lägg till ett nytt lager i Visio Diagram (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Layers/addnewlayer.rb)
