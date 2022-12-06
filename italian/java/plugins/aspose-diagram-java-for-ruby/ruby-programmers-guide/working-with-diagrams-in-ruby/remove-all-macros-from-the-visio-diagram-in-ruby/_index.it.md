---
title: Rimuovi tutte le macro da Visio Diagram in Ruby
type: docs
weight: 50
url: /it/java/remove-all-macros-from-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Rimuovi tutte le macro dal Visio Diagram**
 Per rimuovere tutte le macro dal Visio Diagram utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**Rimuovi tutte le macro dal diagramma** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# remove all macros

diagram.setVbProjectData(nil)

\# Save as VDX

diagram.save(data_dir + "RemoveAllMacros.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Removed all macros from diagram successfully!"

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Rimuovi tutte le macro da Visio Diagram (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/removeallmacrosfromdiagram.rb)
