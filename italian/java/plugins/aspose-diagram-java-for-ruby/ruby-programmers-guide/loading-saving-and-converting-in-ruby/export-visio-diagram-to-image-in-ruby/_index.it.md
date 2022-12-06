---
title: Esporta Visio Diagram in Immagine in Ruby
type: docs
weight: 30
url: /it/java/export-visio-diagram-to-image-in-ruby/
---
## **Aspose.Diagram - Esporta Visio Diagram in immagine**
 Per esportare Visio Diagram nell'immagine utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**Esporta in immagine** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as PNG

diagram.save(data_dir + "Diagram.png", Rjb::import('com.aspose.diagram.SaveFileFormat').PNG)

puts "Exported visio diagram to PNG."

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Esporta Visio Diagram in Immagine (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoimage.rb)
