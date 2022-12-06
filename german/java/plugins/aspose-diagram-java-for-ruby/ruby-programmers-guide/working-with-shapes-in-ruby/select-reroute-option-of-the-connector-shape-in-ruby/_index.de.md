---
title: Wählen Sie die Umleitungsoption der Verbindungsform in Ruby
type: docs
weight: 90
url: /de/java/select-reroute-option-of-the-connector-shape-in-ruby/
---
## **Aspose.Diagram - Wählen Sie die Umleitungsoption der Verbinderform aus**
 Um die Umleitungsoption der Verbinderform auszuwählen, verwenden Sie**Aspose.Diagram Java für Rubin** , einfach aufrufen**Wählen Sie Umleitungsoption** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

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
## **Laufcode herunterladen**
 Download**Wählen Sie die Umleitungsoption der Verbinderform (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/selectrerouteoption.rb)
