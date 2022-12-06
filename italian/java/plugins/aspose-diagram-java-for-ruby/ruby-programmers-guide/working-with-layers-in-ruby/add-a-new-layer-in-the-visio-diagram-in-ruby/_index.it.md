---
title: Aggiungi un nuovo livello nel Visio Diagram in Ruby
type: docs
weight: 10
url: /it/java/add-a-new-layer-in-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Aggiungi un nuovo livello**
 Per aggiungere un nuovo livello utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**Aggiungi nuovo livello** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

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
## **Scarica il codice in esecuzione**
 Scarica**Aggiungi un nuovo livello nel Visio Diagram (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Layers/addnewlayer.rb)
