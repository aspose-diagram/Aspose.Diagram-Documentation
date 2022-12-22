---
title: Leggi Visio Shape Data in Ruby
type: docs
weight: 50
url: /it/java/read-visio-shape-data-in-ruby/
---
## **Aspose.Diagram - Leggi tutte le proprietà della forma**
 Per leggere tutte le proprietà della forma utilizzando**Aspose.Diagram Java per Rubino** , chiamata**read_all_shape_properties** metodo di**ReadShapeData** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 sicuramente leggi_tutto_proprietà_forma()

 dati_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/dati/'

 # Crea un'istanza di Diagram

 diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

 forme = diagram.getPages().getPage(0).getShapes()



 io = 0

 mentre io< shapes.getCount()

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

{{< /highlight >}}
## **Aspose.Diagram - Leggere una proprietà Shape per nome**
 Per leggere una proprietà Shape per nome utilizzando**Aspose.Diagram Java per Rubino** , chiamata**read_shape_property_by_name** metodo di**ReadShapeData** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 sicuramente leggi_forma_proprietà_di_nome()

 dati_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/dati/'

 # Crea un'istanza di Diagram

 diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

 forme = diagram.getPages().getPage(0).getShapes()



 io = 0

 mentre io< shapes.getCount()

        shape = shapes.get(i)

        if shape.getName() == "Process"

            property = shape.getProps().getProp("Cost")

            puts property.getLabel().getValue() + ": " + property.getValue().getVal()

        end

        i +=1

    end

end

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Leggi Visio Dati forma (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/readshapedata.rb)
