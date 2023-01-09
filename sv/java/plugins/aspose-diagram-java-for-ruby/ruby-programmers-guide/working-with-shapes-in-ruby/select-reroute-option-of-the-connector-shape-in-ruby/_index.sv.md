---
title: Välj omdirigeringsalternativ för Connector Shape i Ruby
type: docs
weight: 90
url: /sv/java/select-reroute-option-of-the-connector-shape-in-ruby/
---
## **Aspose.Diagram - Välj omdirigeringsalternativ för anslutningsformen**
 För att välja omdirigeringsalternativ för anslutningsformen med hjälp av**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**Välj RerouteOption** modul. Här kan du se exempelkod.

**Ruby kod**

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
## **Ladda ner Running Code**
 Ladda ner**Välj omdirigeringsalternativ för anslutningsformen (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/selectrerouteoption.rb)
