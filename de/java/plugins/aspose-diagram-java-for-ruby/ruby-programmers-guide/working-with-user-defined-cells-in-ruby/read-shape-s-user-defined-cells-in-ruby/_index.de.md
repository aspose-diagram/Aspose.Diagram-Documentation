---
title: Lesen Sie die benutzerdefinierten Zellen von Shape in Ruby
type: docs
weight: 20
url: /de/java/read-shape-s-user-defined-cells-in-ruby/
---
## **Aspose.Diagram – Benutzerdefinierte Zellen von Shape lesen**
 So lesen Sie die benutzerdefinierten Zellen von Shape mit**Aspose.Diagram Java für Rubin** , einfach aufrufen**ReadUserDefinedCells** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 Daten_dir = Datei.dirname(Datei.dirname(Datei.dirname(Datei.dirname(__DATEI__)))) + '/data/'

\# Instanz von Diagram erstellen

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "UserDefinedCells.vdx")

Formen = diagram.getPages().getPage("Flow 1").getShapes()

ich = 0

 während ich< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process"

        users = shape.getUsers()

        j = 0

        while j < users.getCount()

            user = users.get(j)

            puts user.getName() + ": " + user.getValue().getVal()

            j +=1

        end

        break

    end

    i +=1

end

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Benutzerdefinierte Zellen von Shape lesen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/readuserdefinedcells.rb)
