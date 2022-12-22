---
title: Exportera Visio Diagram till Image in Ruby
type: docs
weight: 30
url: /sv/java/export-visio-diagram-to-image-in-ruby/
---
## **Aspose.Diagram - Exportera Visio Diagram till bild**
 För att exportera Visio Diagram till bild med hjälp av**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**ExportToImage** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as PNG

diagram.save(data_dir + "Diagram.png", Rjb::import('com.aspose.diagram.SaveFileFormat').PNG)

puts "Exported visio diagram to PNG."

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Exportera Visio Diagram till bild (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoimage.rb)
