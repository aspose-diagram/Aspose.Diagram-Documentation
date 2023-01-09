---
title: Récupérer les informations de forme Visio dans Ruby
type: docs
weight: 70
url: /fr/java/retrieve-visio-shape-information-in-ruby/
---
## **Aspose.Diagram - Récupérer les informations de forme Visio**
 Pour récupérer les informations de forme Visio à l'aide de**Aspose.Diagram Java pour rubis** , invoquez simplement**GetShapeInfo** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 Les données_dir = File.dirname(File.dirname(File.dirname(File.dirname(__DOSSIER__)))) + '/données/'

\# Créer une instance de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Dessin.vsd")

formes = diagram.getPages().getPage(0).getShapes()

je = 0

 alors que je< shapes.getCount()

    shape = shapes.get(i)

    # Display information about the shapes

    puts "Shape ID : " + shape.getID().to_s

    puts "Name : " + shape.getName().to_s

    puts "Master Shape : " + shape.getMaster().getName().to_s

    i +=1

end

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Récupérer les informations de forme Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/getshapeinfo.rb)
