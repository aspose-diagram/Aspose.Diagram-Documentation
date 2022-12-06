---
title: Impostare l'aspetto della forma del tipo di connettore in Visio in Ruby
type: docs
weight: 100
url: /it/java/set-appearance-of-the-connector-type-shape-in-visio-in-ruby/
---
## **Aspose.Diagram - Impostare l'aspetto della forma del tipo di connettore in Visio**
 Per impostare l'aspetto della forma del tipo di connettore in Visio utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**ImpostaFormaAspetto** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Access a particular page

page = diagram.getPages().getPage("Flow 1")

\# get a particular connector shape

shape = page.getShapes().getShape(1)

\# set dynamic connector appearance

shape.setConnectorsType(Rjb::import('com.aspose.diagram.ConnectorsTypeValue').STRAIGHT_LINES)

\# Save diagram

diagram.save(data_dir + "SetShapeAppearance.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set appearnce of the connector type shape."

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Impostare l'aspetto della forma del tipo di connettore in Visio (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapeappearance.rb)
