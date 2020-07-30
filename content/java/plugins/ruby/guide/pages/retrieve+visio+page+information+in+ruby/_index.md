---
title : "Retrieve Visio Page Information in Ruby" 
description : "" 
weight : 20118 
toc : false
type: docs
url: /java/plugins/ruby/guide/pages/retrieve+visio+page+information+in+ruby/
---

# Aspose.Diagram for Java : Retrieve Visio Page Information in Ruby


## Aspose.Diagram - Retrieve Visio Page Information

To Retrieve Visio Page Information using **Aspose.Diagram Java for Ruby**, simply invoke **GetPageInfo** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Call the diagram constructor to load diagram from a VSD filediagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")#page = diagram.getPages().getPage(page\_id)page = diagram.getPages().getPage(0)puts "Page ID : " + page.getName().to\_s

## Download Running Code

Download **Retrieve Visio Page Information (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/getpageinfo.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Pages/getpageinfo.rb)

