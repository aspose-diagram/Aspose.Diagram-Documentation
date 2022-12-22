---
title: Export Visio Diagram to XAML in Ruby
type: docs
weight: 60
url: /de/java/export-visio-diagram-to-xaml-in-ruby/
---
## **Aspose.Diagram - Export Visio Diagram to XAML**
To Export Visio Diagram to XAML using **Aspose.Diagram Java für Rubin** , einfach aufrufen**ExportToXaml** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as XAML

diagram.save(data_dir + "Diagram.xaml", Rjb::import('com.aspose.diagram.SaveFileFormat').XAML)

puts "Exported visio diagram to XAML."

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Export Visio Diagram to XAML (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoxaml.rb)
