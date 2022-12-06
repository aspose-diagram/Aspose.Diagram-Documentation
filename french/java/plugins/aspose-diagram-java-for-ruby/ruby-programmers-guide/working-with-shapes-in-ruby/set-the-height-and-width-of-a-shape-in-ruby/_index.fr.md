---
title: Définir la hauteur et la largeur d'une forme en Ruby
type: docs
weight: 120
url: /fr/java/set-the-height-and-width-of-a-shape-in-ruby/
---
## **Aspose.Diagram - Définir la hauteur et la largeur d'une forme**
 Pour définir la hauteur et la largeur d'une forme à l'aide**Aspose.Diagram Java pour rubis** , invoquez simplement**DéfinirFormeHauteurEtLargeur** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 Les données_dir = File.dirname(File.dirname(File.dirname(File.dirname(__DOSSIER__)))) + '/données/'

\# Créer une instance de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Dessin.vsd")

formes = diagram.getPages().getPage(0).getShapes()

je = 0

 alors que je< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process" && shape.getID() == 1

        shape.setWidth(2 * shape.getXForm().getWidth().getValue())

        shape.setHeight(2 * shape.getXForm().getHeight().getValue())

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "SetShapeHeightAndWidth.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set height and width of shape."

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Définir la hauteur et la largeur d'une forme (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapeheightandwidth.rb)
