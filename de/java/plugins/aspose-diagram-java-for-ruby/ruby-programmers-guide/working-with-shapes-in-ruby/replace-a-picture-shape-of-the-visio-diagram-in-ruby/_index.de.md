---
title: Ersetzen Sie eine Bildform von Visio Diagram in Ruby
type: docs
weight: 60
url: /de/java/replace-a-picture-shape-of-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Ersetzen Sie eine Bildform von Visio Diagram**
 So ersetzen Sie eine Bildform von Visio mit Diagram**Aspose.Diagram Java für Rubin** , einfach aufrufen**Bildform ersetzen** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 Daten_dir = Datei.dirname(Datei.dirname(Datei.dirname(Datei.dirname(__DATEI__)))) + '/data/'

\# Instanz von Diagram erstellen

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Bild in Bytes-Array konvertieren

fi = Rjb::import('java.io.File').new(data_dir + "star.png")

file_content = Rjb::import('java.nio.file.Files').readAllBytes(fi.toPath())

Formen = diagram.getPages().getPage("Flow 1").getShapes()

ich = 0

 während ich< shapes.getCount()

    shape = shapes.get(i)

    # Filter shapes by type Foreign

    if shape.getType() == Rjb::import('com.aspose.diagram.TypeValue').FOREIGN

        # replace picture shape

        shape.getForeignData().setValue(file_content)

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "ReplacePictureShape.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Replaced picture shape successfully!"

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Ersetzen Sie eine Bildform des Visio Diagram (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/replacepictureshape.rb)
