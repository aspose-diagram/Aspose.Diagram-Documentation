---
title: Holen Sie sich ein Seitenobjekt aus Visio Drawing in Ruby
type: docs
weight: 10
url: /de/java/get-a-page-object-from-visio-drawing-in-ruby/
---
## **Aspose.Diagram – Abrufen eines Seitenobjekts nach ID**
 So erhalten Sie ein Seitenobjekt nach ID mit**Aspose.Diagram Java für Rubin** , Anruf**get_page_object_by_id** Methode von**GetPageObject** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

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
## **Aspose.Diagram – Abrufen eines Seitenobjekts nach Name**
 So erhalten Sie ein Seitenobjekt anhand des Namens mit**Aspose.Diagram Java für Rubin** , Anruf**get_page_object_by_name** Methode von**GetPageObject** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

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
## **Laufcode herunterladen**
 Download**Abrufen eines Seitenobjekts aus Visio-Zeichnung (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/getpageobject.rb)
