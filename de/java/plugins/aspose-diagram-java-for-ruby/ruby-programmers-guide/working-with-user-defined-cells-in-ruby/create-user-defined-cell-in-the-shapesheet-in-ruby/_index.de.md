---
title: Erstellen Sie eine benutzerdefinierte Zelle im ShapeSheet in Ruby
type: docs
weight: 10
url: /de/java/create-user-defined-cell-in-the-shapesheet-in-ruby/
---
## **Aspose.Diagram – Benutzerdefinierte Zelle im ShapeSheet erstellen**
 So erstellen Sie eine benutzerdefinierte Zelle im ShapeSheet mit**Aspose.Diagram Java für Rubin** , einfach aufrufen**CreateUserDefinedCell** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 Daten_dir = Datei.dirname(Datei.dirname(Datei.dirname(Datei.dirname(__DATEI__)))) + '/data/'

\# Instanz von Diagram erstellen

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

Seiten = diagram.getPages()

ich = 0

 während ich< pages.getCount()

    page = pages.get(i)

    shapes = page.getShapes()

    j = 0

    while j < shapes.getCount()

        shape = shapes.get(j)

        if shape.getNameU() == "Process"

            # Initialize user object

            user = Rjb::import('com.aspose.diagram.User').new

            user.setName("UserDefineCell")

            user.getValue().setVal("800")

            # Add user-defined cell

            shape.getUsers().add(user)

        end

        j +=1

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "UserDefinedCells.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Created User-defined Cell in the ShapeSheet."

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Benutzerdefinierte Zelle im ShapeSheet erstellen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/createuserdefinedcell.rb)
