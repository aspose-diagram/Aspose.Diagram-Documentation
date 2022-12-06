---
title: Rufen Sie benutzerdefinierte Zellen aus Shapesheet in Ruby ab
type: docs
weight: 30
url: /de/java/retrieve-user-defined-cells-from-shapesheet-in-ruby/
---
## **Aspose.Diagram – Benutzerdefinierte Zellen aus Shapesheet abrufen**
 So rufen Sie benutzerdefinierte Zellen aus Shapesheet ab**Aspose.Diagram Java für Rubin** , einfach aufrufen**GetUserDefinedCells** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 Daten_dir = Datei.dirname(Datei.dirname(Datei.dirname(Datei.dirname(__DATEI__)))) + '/data/'

\# Instanz von Diagram erstellen

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "UserDefinedCells.vdx")

Seiten = diagram.getPages()

Zählung = 0

 während zählen< pages.getCount()

    page = pages.get(count)

    shapes = page.getShapes()

    i = 0

    while i < shapes.getCount()

        shape = shapes.get(i)

        if shape.getNameU() == "Process"

            users = shape.getUsers()

            j = 0

            while j < users.getCount()

                user = users.get(j)

                            puts "Name: " + user.getNameU() + " Value: " + user.getValue().getVal() + " Prompt: " + user.getPrompt().getValue()

                j +=1

            end

            break

        end

        i +=1

    end

    count +=1

end

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Benutzerdefinierte Zellen aus Shapesheet abrufen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/getuserdefinedcells.rb)
