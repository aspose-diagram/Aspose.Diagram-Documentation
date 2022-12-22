---
title: Lesen Sie Visio Shape-Daten in Ruby
type: docs
weight: 50
url: /de/java/read-visio-shape-data-in-ruby/
---
## **Aspose.Diagram – Alle Shape-Eigenschaften lesen**
 So lesen Sie alle Formeigenschaften mit**Aspose.Diagram Java für Rubin** , Anruf**read_all_shape_properties** Methode von**ReadShapeData** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 auf jeden Fall lesen_alle_shape_properties()

 Daten_dir = Datei.dirname(Datei.dirname(Datei.dirname(Datei.dirname(__DATEI__)))) + '/data/'

 # Instanz von Diagram erstellen

 diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

 Formen = diagram.getPages().getPage(0).getShapes()



 ich = 0

 während ich< shapes.getCount()

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
## **Aspose.Diagram – Lesen Sie eine Shape-Eigenschaft nach Namen**
 So lesen Sie eine Formeigenschaft nach Namen mit**Aspose.Diagram Java für Rubin** , Anruf**read_shape_property_by_name** Methode von**ReadShapeData** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 auf jeden Fall lesen_Form_Eigentum_durch_Name()

 Daten_dir = Datei.dirname(Datei.dirname(Datei.dirname(Datei.dirname(__DATEI__)))) + '/data/'

 # Instanz von Diagram erstellen

 diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

 Formen = diagram.getPages().getPage(0).getShapes()



 ich = 0

 während ich< shapes.getCount()

        shape = shapes.get(i)

        if shape.getName() == "Process"

            property = shape.getProps().getProp("Cost")

            puts property.getLabel().getValue() + ": " + property.getValue().getVal()

        end

        i +=1

    end

end

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Visio Formdaten lesen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/readshapedata.rb)
