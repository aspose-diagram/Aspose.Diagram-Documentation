---
title: Skaffa ett sidobjekt från Visio Rita i Ruby
type: docs
weight: 10
url: /sv/java/get-a-page-object-from-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Hämta ett sidobjekt med ID**
 För att få ett sidobjekt efter ID med hjälp av**Aspose.Diagram Java för Ruby** , ringa upp**get_page_object_by_id** metod av**GetPageObject** modul. Här kan du se exempelkod.

**Ruby kod**

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
## **Aspose.Diagram - Få ett sidobjekt efter namn**
 För att få ett sidobjekt efter namn med hjälp av**Aspose.Diagram Java för Ruby** , ringa upp**get_page_object_by_name** metod av**GetPageObject** modul. Här kan du se exempelkod.

**Ruby kod**

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
## **Ladda ner Running Code**
 Ladda ner**Skaffa ett sidobjekt från Visio Drawing (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/getpageobject.rb)
