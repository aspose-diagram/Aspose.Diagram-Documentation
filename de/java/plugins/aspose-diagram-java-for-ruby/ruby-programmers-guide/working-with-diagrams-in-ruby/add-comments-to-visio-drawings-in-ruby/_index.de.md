---
title: Kommentare zu Visio Zeichnungen in Ruby hinzufügen
type: docs
weight: 40
url: /de/java/add-comments-to-visio-drawings-in-ruby/
---
## **Aspose.Diagram - Kommentare zu Visio Zeichnungen hinzufügen**
 Um Kommentare zu Visio-Zeichnungen hinzuzufügen, verwenden Sie**Aspose.Diagram Java für Rubin** , einfach aufrufen**AddCommentToDiagram** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Add comment

diagram.getPages().getPage(0).addComment(7.205905511811023, 3.880708661417323, "test@")

\# Save as VDX

diagram.save(data_dir + "AddComment.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Added comment successfully!"

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Kommentare zu Visio Zeichnungen hinzufügen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/addcommenttodiagram.rb)
