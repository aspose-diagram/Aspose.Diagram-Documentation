---
title: Recupera celle definite dall'utente da Shapesheet in Ruby
type: docs
weight: 30
url: /it/java/retrieve-user-defined-cells-from-shapesheet-in-ruby/
---
## **Aspose.Diagram - Recupera celle definite dall'utente da Shapesheet**
 Per recuperare celle definite dall'utente da Shapesheet utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**GetUserDefinedCells** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 dati_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/dati/'

\# Crea un'istanza di Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "UserDefinedCells.vdx")

pagine = diagram.getPages()

contare = 0

 mentre conta< pages.getCount()

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
## **Scarica il codice in esecuzione**
 Scarica**Recupera celle definite dall'utente da foglio di forma (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/getuserdefinedcells.rb)
