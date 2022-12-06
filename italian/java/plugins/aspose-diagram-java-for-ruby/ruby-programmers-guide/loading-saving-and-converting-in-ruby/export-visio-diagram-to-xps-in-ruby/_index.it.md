---
title: Export Visio Diagram to XPS in Ruby
type: docs
weight: 80
url: /it/java/export-visio-diagram-to-xps-in-ruby/
---
## **Aspose.Diagram - Export Visio Diagram to XPS**
To Export Visio Diagram to XPS using **Aspose.Diagram Java per Rubino** , semplicemente invocare**ExportToXps** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as XPS

diagram.save(data_dir + "Diagram.xps", Rjb::import('com.aspose.diagram.SaveFileFormat').XPS)

puts "Exported visio diagram to XPS."

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Export Visio Diagram to XPS (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoxps.rb)
