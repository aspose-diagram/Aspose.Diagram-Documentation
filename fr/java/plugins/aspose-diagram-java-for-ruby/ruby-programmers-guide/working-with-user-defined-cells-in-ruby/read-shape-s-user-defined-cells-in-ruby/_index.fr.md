---
title: Lire les cellules définies par l'utilisateur de Shape dans Ruby
type: docs
weight: 20
url: /fr/java/read-shape-s-user-defined-cells-in-ruby/
---
## **Aspose.Diagram - Lire les cellules définies par l'utilisateur de la forme**
 Pour lire les cellules définies par l'utilisateur de Shape à l'aide**Aspose.Diagram Java pour rubis** , invoquez simplement**ReadUserDefinedCells** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 Les données_dir = File.dirname(File.dirname(File.dirname(File.dirname(__DOSSIER__)))) + '/données/'

\# Créer une instance de Diagram

diagram = Rjb :: import('com.aspose.diagram.Diagram').new(data_dir + "UserDefinedCells.vdx")

formes = diagram.getPages().getPage("Flux 1").getShapes()

je = 0

 alors que je< shapes.getCount()

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
## **Télécharger le code d'exécution**
 Télécharger**Lire les cellules définies par l'utilisateur de Shape (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/readuserdefinedcells.rb)
