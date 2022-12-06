---
title: Seleziona l'opzione di reindirizzamento della forma del connettore in Ruby
type: docs
weight: 90
url: /it/java/select-reroute-option-of-the-connector-shape-in-ruby/
---
## **Aspose.Diagram - Selezionare l'opzione di reindirizzamento della forma del connettore**
 Per selezionare l'opzione di reindirizzamento della forma del connettore utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**Selezionare Reindirizza opzione** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Access a particular page

page = diagram.getPages().getPage("Flow 1")

\# get a particular connector shape

shape = page.getShapes().getShape(1)

\# set reroute option

shape.getLayout().getConFixedCode().setValue(Rjb::import('com.aspose.diagram.ConFixedCodeValue').NEVER_REROUTE)

\# Save diagram

diagram.save(data_dir + "SelectRerouteOption.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Seleted reroute option of the connector shape."

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Selezionare l'opzione di reindirizzamento della forma del connettore (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/selectrerouteoption.rb)
