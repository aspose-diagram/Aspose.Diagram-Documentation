---
title: Lägg till stöd för dynamiska nät och anslutningspunkter i Ruby
type: docs
weight: 10
url: /sv/java/add-support-of-dynamic-grids-and-connection-points-in-ruby/
---
## **Aspose.Diagram - Lägg till stöd för dynamiska nät och anslutningspunkter**
 För att lägga till stöd för dynamiska nät och anslutningspunkter med hjälp av**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**AddDynamic GridsAndConnectionPoints** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# get window object by index

window = diagram.getWindows().get(0)

\# check dynamic grid option

window.setDynamicGridEnabled(1)

\# check connection points option

window.setShowConnectionPoints(1)

\# Save as VDX

diagram.save(data_dir + "AddDynamicGridsAndConnectionPoints.vsx", Rjb::import('com.aspose.diagram.SaveFileFormat').VSX)

puts "Added Support of Dynamic Grids and Connection Points in the Visio Drawings."

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Lägg till stöd för dynamiska nät och anslutningspunkter (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/adddynamicgridsandconnectionpoints.rb)
