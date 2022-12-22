---
title: Abrufen von Fensterelementen aus der Zeichnung Visio in Ruby
type: docs
weight: 30
url: /de/java/retrieve-window-elements-from-the-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Abrufen von Fensterelementen aus der Visio-Zeichnung**
 Zum Abrufen von Fensterelementen aus der Visio-Zeichnung mit**Aspose.Diagram Java für Rubin** , einfach aufrufen**GetWindowElements** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 Daten_dir = Datei.dirname(Datei.dirname(Datei.dirname(Datei.dirname(__DATEI__)))) + '/data/'

\# Instanz von Diagram erstellen

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

Fenster = diagram.getWindows()

ich = 0

 während ich< windows.getCount()

    window = windows.get(i)

    puts "ID: " + window.getID().to_s

    puts "Type: " + window.getWindowType().to_s

    puts "Window height: " + window.getWindowHeight().to_s

    puts "Window width: " + window.getWindowWidth().to_s

    puts "Window state: " + window.getWindowState().to_s

    i +=1

end

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Abrufen von Fensterelementen aus der Zeichnung Visio (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/getwindowelements.rb)
