---
title: Retrieve Visio Page Information in Ruby
type: docs
weight: 30
url: /java/retrieve-visio-page-information-in-ruby/
---

## **Aspose.Diagram - Retrieve Visio Page Information**
To Retrieve Visio Page Information using **Aspose.Diagram Java for Ruby**, simply invoke **GetPageInfo** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

#page = diagram.getPages().getPage(page_id)

page = diagram.getPages().getPage(0)

puts "Page ID : " + page.getName().to_s

{{< /highlight >}}
## **Download Running Code**
Download **Retrieve Visio Page Information (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/getpageinfo.rb)
