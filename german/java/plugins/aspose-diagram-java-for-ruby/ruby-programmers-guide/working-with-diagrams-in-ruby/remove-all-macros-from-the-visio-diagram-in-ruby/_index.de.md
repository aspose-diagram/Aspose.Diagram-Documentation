---
title: Entfernen Sie alle Makros aus Visio Diagram in Ruby
type: docs
weight: 50
url: /de/java/remove-all-macros-from-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Entfernen Sie alle Makros aus Visio Diagram**
 So entfernen Sie alle Makros aus der Visio Diagram mit**Aspose.Diagram Java für Rubin** , einfach aufrufen**RemoveAllMacrosFromDiagram** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

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
## **Laufcode herunterladen**
 Download**Entfernen Sie alle Makros von Visio Diagram (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/removeallmacrosfromdiagram.rb)
