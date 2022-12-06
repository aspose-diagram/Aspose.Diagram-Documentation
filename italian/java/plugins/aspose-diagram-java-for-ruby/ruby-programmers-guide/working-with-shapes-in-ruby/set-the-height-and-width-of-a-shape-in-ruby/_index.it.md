---
title: Imposta l'altezza e la larghezza di una forma in Ruby
type: docs
weight: 120
url: /it/java/set-the-height-and-width-of-a-shape-in-ruby/
---
## **Aspose.Diagram - Imposta l'altezza e la larghezza di una forma**
 Per impostare l'altezza e la larghezza di una forma utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**SetShapeHeightAndWidth** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 dati_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/dati/'

\# Crea un'istanza di Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

forme = diagram.getPages().getPage(0).getShapes()

io = 0

 mentre io< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process" && shape.getID() == 1

        shape.setWidth(2 * shape.getXForm().getWidth().getValue())

        shape.setHeight(2 * shape.getXForm().getHeight().getValue())

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "SetShapeHeightAndWidth.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set height and width of shape."

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Impostare l'altezza e la larghezza di una forma (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapeheightandwidth.rb)
