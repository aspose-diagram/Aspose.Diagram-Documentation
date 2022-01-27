---
title: Insert a New Blank Page into a Visio Drawing in Ruby
type: docs
weight: 20
url: /java/insert-a-new-blank-page-into-a-visio-drawing-in-ruby/
---

## **Aspose.Diagram - Insert a New Blank Page into a Visio Drawing**
To Insert a New Blank Page into a Visio Drawing using **Aspose.Diagram Java for Ruby**, simply invoke **AddPage** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

 def initialize()

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    # Get max page ID

    max_page_id = get_max_page_id(diagram)

    # Initialize a new page object

    new_page = Rjb::import('com.aspose.diagram.Page').new

    # Set name

    new_page.setName("new page")



    # Set page ID

    new_page.setID(max_page_id + 1)

    # Or try the Page constructor

    # Page newPage = new Page(MaxPageId + 1);

    # Add a new blank page

    diagram.getPages().add(new_page)

    # Save diagram

    diagram.save(data_dir + "NewPage_Output.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

    puts "Added new page."

end

def get_max_page_id(diagram)

    max = diagram.getPages().getPage(0).getID()

    i = 1

    while i < diagram.getPages().getCount()

        if max < diagram.getPages().getPage(i).getID()

            max = diagram.getPages().getPage(i).getID()

        end

        i +=1

    end

    return max

end

{{< /highlight >}}
## **Download Running Code**
Download **Insert a New Blank Page into a Visio Drawing (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/addpage.rb)
