---
title: Läs Visio Shape Data i Ruby
type: docs
weight: 50
url: /sv/java/read-visio-shape-data-in-ruby/
---
## **Aspose.Diagram - Läs alla formegenskaper**
 För att läsa alla formegenskaper med hjälp av**Aspose.Diagram Java för Ruby** , ringa upp**read_all_shape_properties** metod av**ReadShapeData** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

 def läs_Allt_shape_properties()

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FIL__)))) + '/data/'

 # Skapa instans av Diagram

 diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

 shapes = diagram.getPages().getPage(0).getShapes()



 i = 0

 medan jag< shapes.getCount()

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
## **Aspose.Diagram - Läs en Shape Property efter namn**
 För att läsa en formegenskap efter namn med hjälp av**Aspose.Diagram Java för Ruby** , ringa upp**read_shape_property_by_name** metod av**ReadShapeData** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

 def läs_form_fast egendom_förbi_namn()

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FIL__)))) + '/data/'

 # Skapa instans av Diagram

 diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

 shapes = diagram.getPages().getPage(0).getShapes()



 i = 0

 medan jag< shapes.getCount()

        shape = shapes.get(i)

        if shape.getName() == "Process"

            property = shape.getProps().getProp("Cost")

            puts property.getLabel().getValue() + ": " + property.getValue().getVal()

        end

        i +=1

    end

end

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Läs Visio Shape Data (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/readshapedata.rb)
