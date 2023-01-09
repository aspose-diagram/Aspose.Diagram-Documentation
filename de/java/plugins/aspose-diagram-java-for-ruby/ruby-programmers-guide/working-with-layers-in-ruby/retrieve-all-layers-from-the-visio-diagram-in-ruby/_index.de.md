---
title: Rufen Sie alle Ebenen von Visio Diagram in Ruby ab
type: docs
weight: 30
url: /de/java/retrieve-all-layers-from-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Alle Ebenen abrufen**
 So rufen Sie alle Ebenen ab mit**Aspose.Diagram Java für Rubin** , einfach aufrufen**GetAllLayers** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 Daten_dir = Datei.dirname(Datei.dirname(Datei.dirname(Datei.dirname(__DATEI__)))) + '/data/'

\# Instanz von Diagram erstellen

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Seite Visio abrufen

Seite = diagram.getPages().getPage(0)

Schichten = page.getPageSheet().getLayers()

ich = 0

 während ich< layers.getCount()

    layer = layers.get(i)

    puts "Name: " + layer.getName().getValue().to_s

    puts "Visibility: " + layer.getVisible().getValue().to_s

    puts "Status: " + layer.getStatus().getValue().to_s



    i +=1

end

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Abrufen aller Ebenen von Visio Diagram (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Layers/getalllayers.rb)
