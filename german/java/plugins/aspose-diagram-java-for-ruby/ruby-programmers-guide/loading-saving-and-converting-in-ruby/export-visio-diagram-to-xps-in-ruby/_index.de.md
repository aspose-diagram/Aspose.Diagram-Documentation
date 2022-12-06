---
title: Export Visio Diagram to XPS in Ruby
type: docs
weight: 80
url: /de/java/export-visio-diagram-to-xps-in-ruby/
---
## **Aspose.Diagram - Export Visio Diagram to XPS**
To Export Visio Diagram to XPS using **Aspose.Diagram Java für Rubin** , einfach aufrufen**ExportToXps** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as XPS

diagram.save(data_dir + "Diagram.xps", Rjb::import('com.aspose.diagram.SaveFileFormat').XPS)

puts "Exported visio diagram to XPS."

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Export Visio Diagram to XPS (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoxps.rb)
