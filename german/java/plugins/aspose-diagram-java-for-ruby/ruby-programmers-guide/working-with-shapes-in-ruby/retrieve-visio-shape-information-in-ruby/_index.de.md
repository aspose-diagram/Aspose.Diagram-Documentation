---
title: Rufen Sie Visio-Shape-Informationen in Ruby ab
type: docs
weight: 70
url: /de/java/retrieve-visio-shape-information-in-ruby/
---
## **Aspose.Diagram - Abrufen von Visio-Shape-Informationen**
 Abrufen von Visio-Shape-Informationen mit**Aspose.Diagram Java für Rubin** , einfach aufrufen**GetShapeInfo** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 Daten_dir = Datei.dirname(Datei.dirname(Datei.dirname(Datei.dirname(__DATEI__)))) + '/data/'

\# Instanz von Diagram erstellen

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

Formen = diagram.getPages().getPage(0).getShapes()

ich = 0

 während ich< shapes.getCount()

    shape = shapes.get(i)

    # Display information about the shapes

    puts "Shape ID : " + shape.getID().to_s

    puts "Name : " + shape.getName().to_s

    puts "Master Shape : " + shape.getMaster().getName().to_s

    i +=1

end

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Visio Forminformationen abrufen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/getshapeinfo.rb)
