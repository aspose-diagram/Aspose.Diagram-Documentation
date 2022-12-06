---
title: Fügen Sie eine neue leere Seite in eine Visio-Zeichnung in Ruby ein
type: docs
weight: 20
url: /de/java/insert-a-new-blank-page-into-a-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Fügen Sie eine neue leere Seite in eine Visio-Zeichnung ein**
 So fügen Sie eine neue leere Seite in eine Visio-Zeichnung ein:**Aspose.Diagram Java für Rubin** , einfach aufrufen**Seite hinzufügen** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 def initialisieren()

 Daten_dir = Datei.dirname(Datei.dirname(Datei.dirname(Datei.dirname(__DATEI__)))) + '/data/'

 Rufen Sie den diagram-Konstruktor auf, um diagram aus einer VSD-Datei zu laden

 diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

 # Maximale Seiten-ID erhalten

 max_Seite_id = erhalten_max_page_id(diagram)

 # Ein neues Seitenobjekt initialisieren

 new_page = Rjb::import('com.aspose.diagram.Page').new

 # Name einsetzen

 new_page.setName("neue Seite")



 # Seiten-ID festlegen

 Neu_page.setID(max_Seiten_ID + 1)

 # Oder versuchen Sie es mit dem Page-Konstruktor

 # Seite neueSeite = neue Seite(MaxPageId + 1);

 # Fügen Sie eine neue leere Seite hinzu

 diagram.getPages().add(neue_Seite)

 # Sparen Sie diagram

 diagram.save(daten_dir + "NeueSeite_Output.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

 puts "Neue Seite hinzugefügt."

Ende

def erhalten_max_page_id(diagram)

max = diagram.getPages().getPage(0).getID()

 ich = 1

 während ich< diagram.getPages().getCount()

        if max < diagram.getPages().getPage(i).getID()

            max = diagram.getPages().getPage(i).getID()

        end

        i +=1

    end

    return max

end

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Einfügen einer neuen leeren Seite in eine Visio-Zeichnung (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/addpage.rb)
