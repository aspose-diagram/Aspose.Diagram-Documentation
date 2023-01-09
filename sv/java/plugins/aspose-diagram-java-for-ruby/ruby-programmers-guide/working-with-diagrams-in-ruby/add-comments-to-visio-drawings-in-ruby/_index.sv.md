---
title: Lägg till kommentarer till Visio Ritningar i Ruby
type: docs
weight: 40
url: /sv/java/add-comments-to-visio-drawings-in-ruby/
---
## **Aspose.Diagram - Lägg till kommentarer till Visio ritningar**
 För att lägga till kommentarer till Visio Ritningar med hjälp av**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**AddCommentToDiagram** modul. Här kan du se exempelkod.

**Ruby kod**

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
## **Ladda ner Running Code**
 Ladda ner**Lägg till kommentarer till Visio Ritningar (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/addcommenttodiagram.rb)
