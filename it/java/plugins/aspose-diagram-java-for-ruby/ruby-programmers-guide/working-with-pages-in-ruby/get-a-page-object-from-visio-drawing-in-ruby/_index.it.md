---
title: Ottieni un oggetto pagina da Visio Drawing in Ruby
type: docs
weight: 10
url: /it/java/get-a-page-object-from-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Ottenere un oggetto della pagina per ID**
 Per ottenere un oggetto pagina per ID utilizzando**Aspose.Diagram Java per Rubino** , chiamata**get_page_object_by_id** metodo di**OttieniOggettoPagina** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

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
## **Aspose.Diagram - Ottenere un oggetto pagina per nome**
 Per ottenere un oggetto pagina per nome utilizzando**Aspose.Diagram Java per Rubino** , chiamata**get_page_object_by_name** metodo di**OttieniOggettoPagina** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

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
## **Scarica il codice in esecuzione**
 Scarica**Ottieni un oggetto pagina dal disegno Visio (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/getpageobject.rb)
