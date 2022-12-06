---
title: Récupérer les informations de page Visio en Ruby
type: docs
weight: 30
url: /fr/java/retrieve-visio-page-information-in-ruby/
---
## **Aspose.Diagram - Récupérer les informations de la page Visio**
 Pour récupérer les informations de la page Visio à l'aide de**Aspose.Diagram Java pour rubis** , invoquez simplement**GetPageInfo** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

# page = diagram.getPages().getPage(page_id)

page = diagram.getPages().getPage(0)

puts "Page ID : " + page.getName().to_s

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Récupérer les informations de la page Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/getpageinfo.rb)
