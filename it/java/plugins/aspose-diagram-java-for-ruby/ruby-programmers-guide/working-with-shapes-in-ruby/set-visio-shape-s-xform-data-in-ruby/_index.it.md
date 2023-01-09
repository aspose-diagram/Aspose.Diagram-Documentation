---
title: Imposta i dati XForm di Visio Shape in Ruby
type: docs
weight: 150
url: /it/java/set-visio-shape-s-xform-data-in-ruby/
---
## **Aspose.Diagram - Imposta i dati XForm di Visio Shape**
 Per impostare i dati XForm di Visio Shape utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**SetShapeXFormData** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 dati_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/dati/'

\# Crea un'istanza di Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

forme = diagram.getPages().getPage(0).getShapes()

io = 0

 mentre io< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "process" && shape.getID() == 1

        shape.getXForm().getPinX().setValue(5)

        shape.getXForm().getPinY().setValue(5)

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "SetShapeXFormData.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set visio shape's XForm data."

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Imposta Visio Dati XForm di Shape (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapexformdata.rb)
