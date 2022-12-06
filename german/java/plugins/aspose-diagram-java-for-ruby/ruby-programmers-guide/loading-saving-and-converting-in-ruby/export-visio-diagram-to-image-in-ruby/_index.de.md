---
title: Exportieren Sie Visio Diagram in Image in Ruby
type: docs
weight: 30
url: /de/java/export-visio-diagram-to-image-in-ruby/
---
## **Aspose.Diagram - Visio Diagram in Bild exportieren**
 So exportieren Sie Visio Diagram in Bild mit**Aspose.Diagram Java für Rubin** , einfach aufrufen**ExportToImage** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as PNG

diagram.save(data_dir + "Diagram.png", Rjb::import('com.aspose.diagram.SaveFileFormat').PNG)

puts "Exported visio diagram to PNG."

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Visio Diagram in Bild exportieren (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoimage.rb)
