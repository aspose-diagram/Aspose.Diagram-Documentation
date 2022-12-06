---
title: Exportieren Sie Visio Diagram als PDF in Ruby
type: docs
weight: 40
url: /de/java/export-visio-diagram-to-pdf-in-ruby/
---
## **Aspose.Diagram - Visio Diagram als PDF exportieren**
 So exportieren Sie Visio Diagram in PDF mit**Aspose.Diagram Java für Rubin** , einfach aufrufen**ExportToPdf** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as PDF file format

diagram.save(data_dir + "Diagram.pdf", Rjb::import('com.aspose.diagram.SaveFileFormat').PDF)

puts "Exported visio diagram to pdf."

{{< /highlight >}}
## **Laufcode herunterladen**
Download**Visio Diagram als PDF exportieren (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttopdf.rb)
