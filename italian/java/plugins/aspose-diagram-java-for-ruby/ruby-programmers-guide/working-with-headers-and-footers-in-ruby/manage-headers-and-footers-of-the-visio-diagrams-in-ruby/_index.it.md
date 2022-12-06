---
title: Gestisci intestazioni e piè di pagina dei diagrammi Visio in Ruby
type: docs
weight: 10
url: /it/java/manage-headers-and-footers-of-the-visio-diagrams-in-ruby/
---
## **Aspose.Diagram - Gestisci intestazioni e piè di pagina dei diagrammi Visio**
 Per gestire intestazioni e piè di pagina dei diagrammi Visio utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**HeadersAndFooters** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# add page number at the right corner of header

diagram.getHeaderFooter().setHeaderRight("&p")

\# set text at the center

diagram.getHeaderFooter().setHeaderCenter("Center of the header")

\# set text at the left side

diagram.getHeaderFooter().setHeaderLeft("Left of the header")

\# add text at the right corner of footer

diagram.getHeaderFooter().setFooterRight("Right of the footer")

\# set text at the center

diagram.getHeaderFooter().setFooterCenter("Center of the footer")

\# set text at the left side

diagram.getHeaderFooter().setFooterLeft("Left of the footer")

\# set header & footer color

diagram.getHeaderFooter().setHeaderFooterColor(Rjb::import('com.aspose.diagram.Color').getRed())

\# set text font properties

diagram.getHeaderFooter().getHeaderFooterFont().setItalic(1)

diagram.getHeaderFooter().getHeaderFooterFont().setUnderline(0)

\# Save diagram

diagram.save(data_dir + "HeadersAndFooters.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Done with headers and footers."

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Gestisci intestazioni e piè di pagina dei diagrammi Visio (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/HeadersAndFooters/headersandfooters.rb)
