---
title: Récupérer toutes les couches du Visio Diagram en Ruby
type: docs
weight: 30
url: /fr/java/retrieve-all-layers-from-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Récupérer toutes les couches**
 Pour récupérer tous les calques à l'aide de**Aspose.Diagram Java pour rubis** , invoquez simplement**Obtenir toutes les couches** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 Les données_dir = File.dirname(File.dirname(File.dirname(File.dirname(__DOSSIER__)))) + '/données/'

\# Créer une instance de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Dessin.vsd")

\# obtenir la page Visio

page = diagram.getPages().getPage(0)

couches = page.getPageSheet().getLayers()

je = 0

 alors que je< layers.getCount()

    layer = layers.get(i)

    puts "Name: " + layer.getName().getValue().to_s

    puts "Visibility: " + layer.getVisible().getValue().to_s

    puts "Status: " + layer.getStatus().getValue().to_s



    i +=1

end

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Récupérer toutes les couches du Visio Diagram (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Layers/getalllayers.rb)
