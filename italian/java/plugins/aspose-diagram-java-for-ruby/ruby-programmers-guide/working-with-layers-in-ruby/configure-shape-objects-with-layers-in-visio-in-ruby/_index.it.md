---
title: Configura gli oggetti Shape con i livelli in Visio in Ruby
type: docs
weight: 20
url: /it/java/configure-shape-objects-with-layers-in-visio-in-ruby/
---
## **Aspose.Diagram - Configura oggetti forma con livelli**
 Per configurare gli oggetti forma con i livelli utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**ConfigureShapeWithLayers** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 dati_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/dati/'

\# Crea un'istanza di Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

forme = diagram.getPages().getPage("Flusso 1").getShapes()

io = 0

 mentre io< shapes.getCount()

    shape = shapes.get(i)

    #puts shape.getName().to_s

    if shape.getName() == "Process"

        # Add shape1 in first two layers. Here "0;1" are indexes of the layers

        layer = shape.getLayerMem()

        layer.getLayerMember().setValue("0;1")

    elsif shape.getName() == "Preparation"

        # Remove shape2 from all the layers

        layer = shape.getLayerMem()

        layer.getLayerMember().setValue("")

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "Layers.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Configured Shape Objects with Layers in Visio."

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Configura oggetti forma con livelli in Visio (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Layers/configureshapewithlayers.rb)
