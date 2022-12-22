---
title: Lire les données de forme Visio dans Ruby
type: docs
weight: 50
url: /fr/java/read-visio-shape-data-in-ruby/
---
## **Aspose.Diagram - Lire toutes les propriétés de forme**
 Pour lire toutes les propriétés de forme à l'aide**Aspose.Diagram Java pour rubis** , appel**read_all_shape_properties** méthode de**LireShapeData** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 définitivement lu_tout_shape_properties()

 Les données_dir = File.dirname(File.dirname(File.dirname(File.dirname(__DOSSIER__)))) + '/données/'

 # Créer une instance de Diagram

 diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Dessin.vsd")

 formes = diagram.getPages().getPage(0).getShapes()



 je = 0

 alors que je< shapes.getCount()

        shape = shapes.get(i)

        if shape.getName() == "Process"

            j = 0

            while j < shape.getProps().getCount()

                property = shape.getProps().get(j)

                puts property.getLabel().getValue() + ": " + property.getValue().getVal()

                j +=1

            end

            break

        end

        i +=1

    end

end

{{< /highlight >}}
## **Aspose.Diagram - Lire une propriété de forme par nom**
 Pour lire une propriété de forme par nom à l'aide**Aspose.Diagram Java pour rubis** , appel**read_shape_property_by_name** méthode de**LireShapeData** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 définitivement lu_forme_propriété_par_Nom()

 Les données_dir = File.dirname(File.dirname(File.dirname(File.dirname(__DOSSIER__)))) + '/données/'

 # Créer une instance de Diagram

 diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Dessin.vsd")

 formes = diagram.getPages().getPage(0).getShapes()



 je = 0

 alors que je< shapes.getCount()

        shape = shapes.get(i)

        if shape.getName() == "Process"

            property = shape.getProps().getProp("Cost")

            puts property.getLabel().getValue() + ": " + property.getValue().getVal()

        end

        i +=1

    end

end

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Lire les données de forme Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/readshapedata.rb)
