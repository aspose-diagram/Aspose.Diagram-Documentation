---
title: Extrahieren Sie alle Bilder aus einer Visio-Seite in Ruby
type: docs
weight: 30
url: /de/java/extract-all-images-from-a-visio-page-in-ruby/
---
## **Aspose.Diagram - Extrahieren Sie alle Bilder von einer Visio-Seite**
 So extrahieren Sie alle Bilder von einer Visio-Seite mit**Aspose.Diagram Java für Rubin** , einfach aufrufen**Bilder extrahieren** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 Daten_dir = Datei.dirname(Datei.dirname(Datei.dirname(Datei.dirname(__DATEI__)))) + '/data/'

\# Instanz von Diagram erstellen

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

Formen = diagram.getPages().getPage("Flow 1").getShapes()

ich = 0

 während ich< shapes.getCount()

    shape = shapes.get(i)

    # Filter shapes by type Foreign

    if shape.getType() == Rjb::import('com.aspose.diagram.TypeValue').FOREIGN

        # create an image file

        fos = Rjb::import('java.io.FileOutputStream').new(data_dir + "Image#{i}.bmp")

        fos.write(shape.getForeignData().getValue())

        fos.close()

    end

    i +=1

end

puts "Extracted images successfully!"

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Alle Bilder aus einer Visio-Seite extrahieren (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/extractimages.rb)
