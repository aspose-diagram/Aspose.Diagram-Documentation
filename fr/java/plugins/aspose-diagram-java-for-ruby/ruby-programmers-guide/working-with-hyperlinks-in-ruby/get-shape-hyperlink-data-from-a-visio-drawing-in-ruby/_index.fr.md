---
title: Obtenir des données de lien hypertexte de forme à partir d'un dessin Visio en Ruby
type: docs
weight: 20
url: /fr/java/get-shape-hyperlink-data-from-a-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Obtenir des données de lien hypertexte de forme**
Pour obtenir des données de lien hypertexte de forme à l'aide**Aspose.Diagram Java pour rubis** , invoquez simplement**GetShapeHyperlinkData** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 Les données_dir = File.dirname(File.dirname(File.dirname(File.dirname(__DOSSIER__)))) + '/données/'

\# Créer une instance de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Hyperlinks.vdx")

\# Obtenir une forme particulière

forme = diagram.getPages().getPage("Flux 1").getShapes().getShape(1)

hyperliens = shape.getHyperlinks()

je = 0

 alors que je< hyperlinks.getCount()

    hyperlink = hyperlinks.get(i)

    puts "Address: " + hyperlink.getAddress().getValue().to_s

    puts "Sub Address: " + hyperlink.getSubAddress().getValue().to_s

    puts "Description: " + hyperlink.getDescription().getValue().to_s

    i +=1

end

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Obtenir des données de lien hypertexte de forme à partir d'un dessin Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Hyperlinks/getshapehyperlinkdata.rb)
