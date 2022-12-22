---
title: Exportera Visio Diagram till XAML i Ruby
type: docs
weight: 60
url: /sv/java/export-visio-diagram-to-xaml-in-ruby/
---
## **Aspose.Diagram - Exportera Visio Diagram till XAML**
För att exportera Visio Diagram till XAML med**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**ExportToXaml** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as XAML

diagram.save(data_dir + "Diagram.xaml", Rjb::import('com.aspose.diagram.SaveFileFormat').XAML)

puts "Exported visio diagram to XAML."

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Exportera Visio Diagram till XAML (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoxaml.rb)
