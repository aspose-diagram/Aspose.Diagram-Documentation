---
title: Exportera Visio Diagram till PDF i Ruby
type: docs
weight: 40
url: /sv/java/export-visio-diagram-to-pdf-in-ruby/
---
## **Aspose.Diagram - Exportera Visio Diagram till PDF**
 För att exportera Visio Diagram till PDF med hjälp av**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**Exportera till pdf** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as PDF file format

diagram.save(data_dir + "Diagram.pdf", Rjb::import('com.aspose.diagram.SaveFileFormat').PDF)

puts "Exported visio diagram to pdf."

{{< /highlight >}}
## **Ladda ner Running Code**
Ladda ner**Exportera Visio Diagram till PDF (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttopdf.rb)
