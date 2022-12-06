---
title: Leggi le celle definite dall'utente di Shape in Ruby
type: docs
weight: 20
url: /it/java/read-shape-s-user-defined-cells-in-ruby/
---
## **Aspose.Diagram - Leggi le celle definite dall'utente di Shape**
 Per leggere le celle definite dall'utente di Shape utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**ReadUserDefinedCells** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 dati_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/dati/'

\# Crea un'istanza di Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "UserDefinedCells.vdx")

forme = diagram.getPages().getPage("Flusso 1").getShapes()

io = 0

 mentre io< shapes.getCount()

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
## **Scarica il codice in esecuzione**
 Scarica**Leggi celle definite dall'utente di Shape (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/readuserdefinedcells.rb)
