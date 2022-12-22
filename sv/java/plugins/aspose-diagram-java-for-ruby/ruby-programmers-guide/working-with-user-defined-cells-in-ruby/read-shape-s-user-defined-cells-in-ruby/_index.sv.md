---
title: Läs Shapes användardefinierade celler i Ruby
type: docs
weight: 20
url: /sv/java/read-shape-s-user-defined-cells-in-ruby/
---
## **Aspose.Diagram - Läs Shapes användardefinierade celler**
 För att läsa Shapes användardefinierade celler med hjälp av**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**ReadUserDefinedCells** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FIL__)))) + '/data/'

\# Skapa instans av Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "UserDefinedCells.vdx")

shapes = diagram.getPages().getPage("Flöde 1").getShapes()

i = 0

 medan jag< shapes.getCount()

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
## **Ladda ner Running Code**
 Ladda ner**Läs Shapes användardefinierade celler (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/readuserdefinedcells.rb)
