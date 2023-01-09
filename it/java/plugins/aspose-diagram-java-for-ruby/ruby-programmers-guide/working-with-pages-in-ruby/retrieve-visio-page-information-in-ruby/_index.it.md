---
title: Recupera le informazioni sulla pagina Visio in Ruby
type: docs
weight: 30
url: /it/java/retrieve-visio-page-information-in-ruby/
---
## **Aspose.Diagram - Recupera Visio Informazioni Pagina**
 Per recuperare le informazioni sulla pagina Visio utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**OttieniInfoPagina** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

# page = diagram.getPages().getPage(page_id)

page = diagram.getPages().getPage(0)

puts "Page ID : " + page.getName().to_s

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Recupera Visio Informazioni sulla pagina (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/getpageinfo.rb)
