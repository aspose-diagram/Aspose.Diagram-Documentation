---
title: Legen Sie die Höhe und Breite einer Form in Ruby fest
type: docs
weight: 120
url: /de/java/set-the-height-and-width-of-a-shape-in-ruby/
---
## **Aspose.Diagram - Legen Sie die Höhe und Breite einer Form fest**
 So stellen Sie die Höhe und Breite einer Form mit ein**Aspose.Diagram Java für Rubin** , einfach aufrufen**SetShapeHeightAndWidth** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 Daten_dir = Datei.dirname(Datei.dirname(Datei.dirname(Datei.dirname(__DATEI__)))) + '/data/'

\# Instanz von Diagram erstellen

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

Formen = diagram.getPages().getPage(0).getShapes()

ich = 0

 während ich< shapes.getCount()

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
## **Laufcode herunterladen**
 Download**Festlegen der Höhe und Breite einer Form (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapeheightandwidth.rb)
