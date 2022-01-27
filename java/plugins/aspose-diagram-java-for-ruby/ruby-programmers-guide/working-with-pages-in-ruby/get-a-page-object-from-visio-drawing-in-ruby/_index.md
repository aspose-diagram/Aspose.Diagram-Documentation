---
title: Get a Page Object from Visio Drawing in Ruby
type: docs
weight: 10
url: /java/get-a-page-object-from-visio-drawing-in-ruby/
---

## **Aspose.Diagram - Getting a Page Object by ID**
To Get a Page Object by ID using **Aspose.Diagram Java for Ruby**, call **get_page_object_by_id** method of **GetPageObject** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

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
## **Aspose.Diagram - Getting a Page Object by Name**
To Get a Page Object by Name using **Aspose.Diagram Java for Ruby**, call **get_page_object_by_name** method of **GetPageObject** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

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
## **Download Running Code**
Download **Get a Page Object from Visio Drawing (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/getpageobject.rb)
