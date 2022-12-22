---
title: Créer une cellule définie par l'utilisateur dans la feuille ShapeSheet en Ruby
type: docs
weight: 10
url: /fr/java/create-user-defined-cell-in-the-shapesheet-in-ruby/
---
## **Aspose.Diagram - Créer une cellule définie par l'utilisateur dans la feuille ShapeSheet**
 Pour créer une cellule définie par l'utilisateur dans la feuille ShapeSheet à l'aide**Aspose.Diagram Java pour rubis** , invoquez simplement**CreateUserDefinedCell** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 Les données_dir = File.dirname(File.dirname(File.dirname(File.dirname(__DOSSIER__)))) + '/données/'

\# Créer une instance de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Dessin.vsd")

pages = diagram.getPages()

je = 0

 alors que je< pages.getCount()

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
## **Télécharger le code d'exécution**
 Télécharger**Créer une cellule définie par l'utilisateur dans la feuille ShapeSheet (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/createuserdefinedcell.rb)
