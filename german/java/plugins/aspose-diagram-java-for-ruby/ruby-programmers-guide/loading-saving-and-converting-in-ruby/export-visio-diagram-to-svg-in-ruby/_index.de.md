---
title: Export Visio Diagram to SVG in Ruby
type: docs
weight: 50
url: /de/java/export-visio-diagram-to-svg-in-ruby/
---
## **Aspose.Diagram - Export Visio Diagram to SVG**
To Export Visio Diagram to SVG using **Aspose.Diagram Java für Rubin** , einfach aufrufen**ExportToSvg** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as SVG

diagram.save(data_dir + "Diagram.svg", Rjb::import('com.aspose.diagram.SaveFileFormat').SVG)

puts "Exported visio diagram to SVG."

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Export Visio Diagram to SVG (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttosvg.rb)
