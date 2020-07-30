---
title : "Get a Page Object from Visio Drawing in Ruby" 
description : "" 
weight : 20116 
toc : false
type: docs
url: /java/plugins/ruby/guide/pages/get+a+page+object+from+visio+drawing+in+ruby/
---

# Aspose.Diagram for Java : Get a Page Object from Visio Drawing in Ruby


## Aspose.Diagram - Getting a Page Object by ID

To Get a Page Object by ID using **Aspose.Diagram Java for Ruby**, call **get\_page\_object\_by\_id** method of **GetPageObject** module. Here you can see example code.

**Ruby Code**

{{< code lang="cs" >}}
def get_page_object_by_id() 
    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file
    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    page_id = 0
    # Get page object by id
    page = diagram.getPages().getPage(page_id)

    puts "Page : " + page.to_string
end
{{< /code >}}

## Aspose.Diagram - Getting a Page Object by Name

To Get a Page Object by Name using **Aspose.Diagram Java for Ruby**, call **get\_page\_object\_by\_name** method of **GetPageObject** module. Here you can see example code.

**Ruby Code**

{{< code lang="cs" >}}
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
{{< /code >}}

## Download Running Code

Download **Get a Page Object from Visio Drawing (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/getpageobject.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Pages/getpageobject.rb)

