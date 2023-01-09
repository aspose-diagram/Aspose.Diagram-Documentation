---
title: Définir les données XForm de la forme Visio dans Ruby
type: docs
weight: 150
url: /fr/java/set-visio-shape-s-xform-data-in-ruby/
---
## **Aspose.Diagram - Définir les données XForm de la forme Visio**
 Pour définir les données XForm de Visio Shape à l'aide de**Aspose.Diagram Java pour rubis** , invoquez simplement**SetShapeXFormData** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 Les données_dir = File.dirname(File.dirname(File.dirname(File.dirname(__DOSSIER__)))) + '/données/'

\# Créer une instance de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Dessin.vsd")

formes = diagram.getPages().getPage(0).getShapes()

je = 0

 alors que je< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "process" && shape.getID() == 1

        shape.getXForm().getPinX().setValue(5)

        shape.getXForm().getPinY().setValue(5)

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "SetShapeXFormData.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set visio shape's XForm data."

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Définir les données XForm de la forme Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapexformdata.rb)
