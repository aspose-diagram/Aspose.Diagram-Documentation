---
title: Unterstützung für dynamische Gitter und Verbindungspunkte in Ruby hinzugefügt
type: docs
weight: 10
url: /de/java/add-support-of-dynamic-grids-and-connection-points-in-ruby/
---
## **Aspose.Diagram – Unterstützung für dynamische Gitter und Verbindungspunkte hinzugefügt**
 So fügen Sie Unterstützung für dynamische Gitter und Verbindungspunkte hinzu**Aspose.Diagram Java für Rubin** , einfach aufrufen**AddDynamicGridsAndConnectionPoints** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

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
## **Laufcode herunterladen**
 Download**Unterstützung für dynamische Gitter und Verbindungspunkte hinzugefügt (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/adddynamicgridsandconnectionpoints.rb)
