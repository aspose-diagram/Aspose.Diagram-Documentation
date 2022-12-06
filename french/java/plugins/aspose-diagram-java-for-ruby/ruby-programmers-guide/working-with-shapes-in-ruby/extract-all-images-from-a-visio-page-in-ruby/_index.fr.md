---
title: Extraire toutes les images d'une page Visio en Ruby
type: docs
weight: 30
url: /fr/java/extract-all-images-from-a-visio-page-in-ruby/
---
## **Aspose.Diagram - Extraire toutes les images d'une page Visio**
 Pour extraire toutes les images d'une page Visio à l'aide**Aspose.Diagram Java pour rubis** , invoquez simplement**Extraire des images** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 Les données_dir = File.dirname(File.dirname(File.dirname(File.dirname(__DOSSIER__)))) + '/données/'

\# Créer une instance de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Dessin.vsd")

formes = diagram.getPages().getPage("Flux 1").getShapes()

je = 0

 alors que je< shapes.getCount()

    shape = shapes.get(i)

    # Filter shapes by type Foreign

    if shape.getType() == Rjb::import('com.aspose.diagram.TypeValue').FOREIGN

        # create an image file

        fos = Rjb::import('java.io.FileOutputStream').new(data_dir + "Image#{i}.bmp")

        fos.write(shape.getForeignData().getValue())

        fos.close()

    end

    i +=1

end

puts "Extracted images successfully!"

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Extraire toutes les images d'une page Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/extractimages.rb)
