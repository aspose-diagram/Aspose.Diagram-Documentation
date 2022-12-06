---
title: Esporta Visio Diagram in XAML in Ruby
type: docs
weight: 60
url: /it/java/export-visio-diagram-to-xaml-in-ruby/
---
## **Aspose.Diagram - Esporta Visio Diagram in XAML**
 Per esportare Visio Diagram in XAML utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**ExportToXaml** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as XAML

diagram.save(data_dir + "Diagram.xaml", Rjb::import('com.aspose.diagram.SaveFileFormat').XAML)

puts "Exported visio diagram to XAML."

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Esporta Visio Diagram in XAML (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoxaml.rb)
