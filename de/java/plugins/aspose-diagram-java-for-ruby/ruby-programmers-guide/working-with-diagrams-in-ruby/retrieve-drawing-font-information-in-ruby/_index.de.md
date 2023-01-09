---
title: Rufen Sie Zeichenschriftinformationen in Ruby ab
type: docs
weight: 30
url: /de/java/retrieve-drawing-font-information-in-ruby/
---
## **Aspose.Diagram – Abrufen von Zeichensatzinformationen**
 So rufen Sie Informationen zu Zeichnungsschriften ab**Aspose.Diagram Java für Rubin** , einfach aufrufen**GetDiagramFontInfo** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 Daten_dir = Datei.dirname(Datei.dirname(Datei.dirname(Datei.dirname(__DATEI__)))) + '/data/'

\# Instanz von Diagram erstellen

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

Schriftarten = diagram.getFonts()

ich = 0

 während ich< fonts.getCount()

    font = fonts.get(i)

    # Display information about the fonts

    puts font.getName()

    i +=1

end

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Zeichnungsschriftinformationen abrufen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/getdiagramfontinfo.rb)
