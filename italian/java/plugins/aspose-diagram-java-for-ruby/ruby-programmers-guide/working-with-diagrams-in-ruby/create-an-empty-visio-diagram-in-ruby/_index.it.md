---
title: Crea un Visio Diagram vuoto in Ruby
type: docs
weight: 10
url: /it/java/create-an-empty-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Crea un vuoto Visio Diagram**
 Per creare un vuoto Visio Diagram utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**Crea diagramma** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new

\# Save as VDX

diagram.save(data_dir + "CreateDiagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Created visio diagram successfully!"

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Crea un vuoto Visio Diagram (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/creatediagram.rb)
