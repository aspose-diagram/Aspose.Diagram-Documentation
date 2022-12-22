---
title: Mostra e nascondi griglie, righelli, guide e interruzioni di pagina di Visio Diagram in Ruby
type: docs
weight: 40
url: /it/java/show-and-hide-grids-rulers-guides-and-page-breaks-of-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Mostra e nascondi griglie, righelli, guide e interruzioni di pagina del Visio Diagram**
Per mostrare e nascondere griglie, righelli, guide e interruzioni di pagina di Visio Diagram utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**MostraNascondiProprietà** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# get window object by index

window = diagram.getWindows().get(0)

\# set visibility of grid

window.setShowGrid(1)

\# set visibility of guides

window.setShowGuides(1)

\# set visibility of rulers

window.setShowRulers(1)

\# set visibility of page breaks

window.setShowPageBreaks(1)

\# save in any supported format

diagram.save(data_dir + "ShowHideProperties.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Show and Hide Grids, Rulers, Guides and Page Breaks of the Visio Diagram."

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Mostra e nascondi griglie, righelli, guide e interruzioni di pagina del Visio Diagram (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/showhideproperties.rb)
