---
title: Erstellen Sie eine leere Visio Diagram in Ruby
type: docs
weight: 10
url: /de/java/create-an-empty-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Erstellen Sie eine leere Visio Diagram**
 Erstellen Sie eine leere Visio mit Diagram**Aspose.Diagram Java für Rubin** , einfach aufrufen**Diagramm erstellen** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new

\# Save as VDX

diagram.save(data_dir + "CreateDiagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Created visio diagram successfully!"

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Erstellen Sie eine leere Visio Diagram (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/creatediagram.rb)
