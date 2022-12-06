---
title: Ändern Sie die Position einer Form in Ruby
type: docs
weight: 10
url: /de/java/change-the-position-of-a-shape-in-ruby/
---
## **Aspose.Diagram - Ändern Sie die Position einer Form**
 So ändern Sie die Position einer Form mit**Aspose.Diagram Java für Rubin** , einfach aufrufen**FormPosition ändern** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 Daten_dir = Datei.dirname(Datei.dirname(Datei.dirname(Datei.dirname(__DATEI__)))) + '/data/'

\# Instanz von Diagram erstellen

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

Formen = diagram.getPages().getPage(0).getShapes()

ich = 0

 während ich< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process" && shape.getID() == 2

        shape.move(1, 1)

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "ChangeShapePosition.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Changed position of a shape."

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Ändern der Position einer Form (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/changeshapeposition.rb)
