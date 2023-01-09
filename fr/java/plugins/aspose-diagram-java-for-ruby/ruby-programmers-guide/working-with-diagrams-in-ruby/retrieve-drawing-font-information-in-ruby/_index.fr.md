---
title: Récupérer les informations de police de dessin dans Ruby
type: docs
weight: 30
url: /fr/java/retrieve-drawing-font-information-in-ruby/
---
## **Aspose.Diagram - Récupérer les informations sur la police de dessin**
 Pour récupérer les informations sur la police de dessin à l'aide de**Aspose.Diagram Java pour rubis** , invoquez simplement**GetDiagramFontInfo** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 Les données_dir = File.dirname(File.dirname(File.dirname(File.dirname(__DOSSIER__)))) + '/données/'

\# Créer une instance de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Dessin.vsd")

polices = diagram.getFonts()

je = 0

 alors que je< fonts.getCount()

    font = fonts.get(i)

    # Display information about the fonts

    puts font.getName()

    i +=1

end

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Récupérer les informations sur la police de dessin (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/getdiagramfontinfo.rb)
