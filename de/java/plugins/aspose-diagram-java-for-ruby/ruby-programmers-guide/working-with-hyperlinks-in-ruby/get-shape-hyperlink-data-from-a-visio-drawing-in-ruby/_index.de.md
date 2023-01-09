---
title: Abrufen von Form-Hyperlink-Daten aus einer Visio-Zeichnung in Ruby
type: docs
weight: 20
url: /de/java/get-shape-hyperlink-data-from-a-visio-drawing-in-ruby/
---
## **Aspose.Diagram – Shape-Hyperlink-Daten abrufen**
So erhalten Sie Form-Hyperlink-Daten mit**Aspose.Diagram Java für Rubin** , einfach aufrufen**GetShapeHyperlinkData** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 Daten_dir = Datei.dirname(Datei.dirname(Datei.dirname(Datei.dirname(__DATEI__)))) + '/data/'

\# Instanz von Diagram erstellen

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Hyperlinks.vdx")

\# Holen Sie sich eine bestimmte Form

Form = diagram.getPages().getPage("Flow 1").getShapes().getShape(1)

hyperlinks = shape.getHyperlinks()

ich = 0

 während ich< hyperlinks.getCount()

    hyperlink = hyperlinks.get(i)

    puts "Address: " + hyperlink.getAddress().getValue().to_s

    puts "Sub Address: " + hyperlink.getSubAddress().getValue().to_s

    puts "Description: " + hyperlink.getDescription().getValue().to_s

    i +=1

end

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Form-Hyperlink-Daten aus einer Visio-Zeichnung abrufen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Hyperlinks/getshapehyperlinkdata.rb)
