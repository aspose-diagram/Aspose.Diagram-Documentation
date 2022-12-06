---
title: Obtenir un objet de page à partir du dessin Visio en Ruby
type: docs
weight: 10
url: /fr/java/get-a-page-object-from-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Obtention d'un objet de page par ID**
 Pour obtenir un objet de page par ID à l'aide de**Aspose.Diagram Java pour rubis** , appel**get_page_object_by_id** méthode de**GetPageObject** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 def get_page_object_by_id() 

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    page_id = 0

    # Get page object by id

    page = diagram.getPages().getPage(page_id)

    puts "Page : " + page.to_string

end

{{< /highlight >}}
## **Aspose.Diagram - Obtenir un objet de page par nom**
 Pour obtenir un objet de page par nom à l'aide**Aspose.Diagram Java pour rubis** , appel**get_page_object_by_name** méthode de**GetPageObject** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 def get_page_object_by_name() 

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    # Set page name

    page_name = "Flow 1"

    # Get page object by name

    page = diagram.getPages().getPage(page_name)

    puts "Page : " + page.to_string

end

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Obtenir un objet de page à partir du dessin Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/getpageobject.rb)
