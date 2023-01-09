---
title: Legen Sie Visio Liniendaten der Form in Ruby fest
type: docs
weight: 140
url: /de/java/set-visio-shape-s-line-data-in-ruby/
---
## **Aspose.Diagram - Legen Sie die Liniendaten der Form Visio fest**
 So stellen Sie die Liniendaten von Visio Shape ein**Aspose.Diagram Java für Rubin** , einfach aufrufen**SetShapeLineData** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 Daten_dir = Datei.dirname(Datei.dirname(Datei.dirname(Datei.dirname(__DATEI__)))) + '/data/'

\# Instanz von Diagram erstellen

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

Formen = diagram.getPages().getPage(0).getShapes()

ich = 0

 während ich< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "rectangle" && shape.getID() == 1

        shape.getLine().getLineColor().setValue(diagram.getPages().getPage(0).getShapes().getShape(1).getFill().getFillForegnd().getValue())

        shape.getLine().getLineWeight().setValue(0.07041666666666667)

        shape.getLine().getRounding().setValue(0.1)

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "SetShapeLineData.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set visio shape's line data."

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Visio Liniendaten der Form festlegen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapelinedata.rb)
