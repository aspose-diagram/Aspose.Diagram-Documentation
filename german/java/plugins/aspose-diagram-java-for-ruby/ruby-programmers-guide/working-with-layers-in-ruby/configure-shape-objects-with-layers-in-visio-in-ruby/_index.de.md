---
title: Konfigurieren Sie Formobjekte mit Ebenen in Visio in Ruby
type: docs
weight: 20
url: /de/java/configure-shape-objects-with-layers-in-visio-in-ruby/
---
## **Aspose.Diagram – Konfigurieren Sie Formobjekte mit Ebenen**
 So konfigurieren Sie Formobjekte mit Ebenen mit**Aspose.Diagram Java für Rubin** , einfach aufrufen**ShapeWithLayers konfigurieren** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 Daten_dir = Datei.dirname(Datei.dirname(Datei.dirname(Datei.dirname(__DATEI__)))) + '/data/'

\# Instanz von Diagram erstellen

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

Formen = diagram.getPages().getPage("Flow 1").getShapes()

ich = 0

 während ich< shapes.getCount()

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
## **Laufcode herunterladen**
 Download**Konfigurieren Sie Formobjekte mit Ebenen in Visio (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Layers/configureshapewithlayers.rb)
