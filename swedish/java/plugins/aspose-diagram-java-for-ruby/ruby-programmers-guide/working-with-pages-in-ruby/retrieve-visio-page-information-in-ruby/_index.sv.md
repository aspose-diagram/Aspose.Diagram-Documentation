---
title: Hämta Visio Sidinformation i Ruby
type: docs
weight: 30
url: /sv/java/retrieve-visio-page-information-in-ruby/
---
## **Aspose.Diagram - Hämta Visio Sidinformation**
 För att hämta Visio Sidinformation med hjälp av**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**GetPageInfo** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

# page = diagram.getPages().getPage(page_id)

page = diagram.getPages().getPage(0)

puts "Page ID : " + page.getName().to_s

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Hämta Visio Sidinformation (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/getpageinfo.rb)
