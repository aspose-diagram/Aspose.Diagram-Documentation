---
title: Rufen Sie Visio-Seiteninformationen in Ruby ab
type: docs
weight: 30
url: /de/java/retrieve-visio-page-information-in-ruby/
---
## **Aspose.Diagram - Abrufen von Visio-Seiteninformationen**
 Abrufen von Visio Seiteninformationen mit**Aspose.Diagram Java für Rubin** , einfach aufrufen**GetPageInfo** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

# page = diagram.getPages().getPage(page_id)

page = diagram.getPages().getPage(0)

puts "Page ID : " + page.getName().to_s

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Abrufen von Visio-Seiteninformationen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/getpageinfo.rb)
