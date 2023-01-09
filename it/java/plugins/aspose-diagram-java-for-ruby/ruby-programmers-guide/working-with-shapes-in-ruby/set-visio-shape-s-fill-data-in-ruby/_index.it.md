---
title: Imposta i dati di riempimento di Visio Shape in Ruby
type: docs
weight: 130
url: /it/java/set-visio-shape-s-fill-data-in-ruby/
---
## **Aspose.Diagram - Imposta Visio Dati di riempimento della forma**
 Per impostare Visio Riempire i dati della forma utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**SetShapeFillData** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 dati_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/dati/'

\# Crea un'istanza di Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

forme = diagram.getPages().getPage(0).getShapes()

io = 0

 mentre io< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "rectangle" && shape.getID() == 1

        shape.getFill().getFillBkgnd().setValue(diagram.getPages().getPage(0).getShapes().getShape(0).getFill().getFillBkgnd().getValue())

        shape.getFill().getFillForegnd().setValue("#ebf8df")

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "SetShapeFillData.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set visio shape's fill data."

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Imposta Visio Dati di riempimento della forma (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapefilldata.rb)
