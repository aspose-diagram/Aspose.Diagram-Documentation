---
title: Ottieni i dati del collegamento ipertestuale Shape da un disegno Visio in Ruby
type: docs
weight: 20
url: /it/java/get-shape-hyperlink-data-from-a-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Ottieni dati collegamento ipertestuale forma**
Per ottenere i dati del collegamento ipertestuale Shape utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**GetShapeHyperlinkData** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 dati_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/dati/'

\# Crea un'istanza di Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Hyperlinks.vdx")

\# Ottieni una forma particolare

shape = diagram.getPages().getPage("Flusso 1").getShapes().getShape(1)

collegamenti ipertestuali = shape.getHyperlinks()

io = 0

 mentre io< hyperlinks.getCount()

    hyperlink = hyperlinks.get(i)

    puts "Address: " + hyperlink.getAddress().getValue().to_s

    puts "Sub Address: " + hyperlink.getSubAddress().getValue().to_s

    puts "Description: " + hyperlink.getDescription().getValue().to_s

    i +=1

end

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Ottieni dati collegamento ipertestuale forma da un disegno Visio (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Hyperlinks/getshapehyperlinkdata.rb)
