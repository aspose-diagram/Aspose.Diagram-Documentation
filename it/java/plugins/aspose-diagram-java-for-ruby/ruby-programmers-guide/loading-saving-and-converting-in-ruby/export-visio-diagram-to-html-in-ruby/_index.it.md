---
title: Export Visio Diagram to HTML in Ruby
type: docs
weight: 20
url: /it/java/export-visio-diagram-to-html-in-ruby/
---
## **Aspose.Diagram - Export Visio Diagram to HTML**
To Export Visio Diagram to HTML using **Aspose.Diagram Java per Rubino** , semplicemente invocare**Esporta in Html** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as Html

diagram.save(data_dir + "Diagram.html", Rjb::import('com.aspose.diagram.SaveFileFormat').HTML)

puts "Exported visio diagram to HTML."

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Export Visio Diagram to HTML (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttohtml.rb)
