---
title: Changer la position d'une forme dans Ruby
type: docs
weight: 10
url: /fr/java/change-the-position-of-a-shape-in-ruby/
---
## **Aspose.Diagram - Modifier la position d'une forme**
 Pour modifier la position d'une forme à l'aide de**Aspose.Diagram Java pour rubis** , invoquez simplement**ChangeShapePosition** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 Les données_dir = File.dirname(File.dirname(File.dirname(File.dirname(__DOSSIER__)))) + '/données/'

\# Créer une instance de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Dessin.vsd")

formes = diagram.getPages().getPage(0).getShapes()

je = 0

 alors que je< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process" && shape.getID() == 2

        shape.move(1, 1)

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "ChangeShapePosition.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Changed position of a shape."

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Modifier la position d'une forme (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/changeshapeposition.rb)
