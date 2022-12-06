---
title: Récupérer des cellules définies par l'utilisateur à partir d'une feuille de forme dans Ruby
type: docs
weight: 30
url: /fr/java/retrieve-user-defined-cells-from-shapesheet-in-ruby/
---
## **Aspose.Diagram - Récupérer des cellules définies par l'utilisateur à partir de la feuille de forme**
 Pour récupérer des cellules définies par l'utilisateur à partir d'une feuille de forme à l'aide**Aspose.Diagram Java pour rubis** , invoquez simplement**GetUserDefinedCells** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 Les données_dir = File.dirname(File.dirname(File.dirname(File.dirname(__DOSSIER__)))) + '/données/'

\# Créer une instance de Diagram

diagram = Rjb :: import('com.aspose.diagram.Diagram').new(data_dir + "UserDefinedCells.vdx")

pages = diagram.getPages()

compter = 0

 tout en comptant< pages.getCount()

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
## **Télécharger le code d'exécution**
 Télécharger**Récupérer des cellules définies par l'utilisateur à partir de la feuille de forme (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/getuserdefinedcells.rb)
