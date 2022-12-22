---
title: Schützen und Entschützen von Diagrammen in Ruby
type: docs
weight: 20
url: /de/java/protect-and-unprotect-diagrams-in-ruby/
---
## **Aspose.Diagram – Diagramme schützen und Schutz aufheben**
 So schützen und entschützen Sie Diagramme mit**Aspose.Diagram Java für Rubin** , einfach aufrufen**ProtectUnprotectDiagram** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

diagram.getDocumentSettings().setProtectBkgnds(1)

diagram.getDocumentSettings().setProtectMasters(1)

diagram.getDocumentSettings().setProtectShapes(1)

diagram.getDocumentSettings().setProtectStyles(1)

\# Save diagram

diagram.save(data_dir + "ProtectUnprotectDiagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Applied protection on diagram successfully!"

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Diagramme zum Schützen und Aufheben des Schutzes (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Protection/protectunprotectdiagram.rb)
