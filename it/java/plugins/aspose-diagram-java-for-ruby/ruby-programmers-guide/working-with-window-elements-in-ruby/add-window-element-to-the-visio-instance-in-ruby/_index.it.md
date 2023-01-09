---
title: Aggiungi l'elemento Window all'istanza Visio in Ruby
type: docs
weight: 20
url: /it/java/add-window-element-to-the-visio-instance-in-ruby/
---
## **Aspose.Diagram - Aggiungi elemento finestra all'istanza Visio**
 Per aggiungere l'elemento finestra all'istanza Visio utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**AggiungiWindowElement** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# initialize window object

window = Rjb::import('com.aspose.diagram.Window').new

\# set window state

window.setWindowState(Rjb::import('com.aspose.diagram.WindowStateValue').MAXIMIZED)

\# set window height

window.setWindowHeight(500)

\# set window width

window.setWindowWidth(500)

\# set window type

window.setWindowType(Rjb::import('com.aspose.diagram.WindowTypeValue').STENCIL)

\# add window object

diagram.getWindows().add(window)

\# save in any supported format

diagram.save(data_dir + "AddWindowElement.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Added window element to the visio instance."

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Aggiungi elemento finestra all'istanza Visio (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/addwindowelement.rb)
