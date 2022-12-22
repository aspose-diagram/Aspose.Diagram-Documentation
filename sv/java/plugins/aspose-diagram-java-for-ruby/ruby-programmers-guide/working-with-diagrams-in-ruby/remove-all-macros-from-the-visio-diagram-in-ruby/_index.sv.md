---
title: Ta bort alla makron från Visio Diagram i Ruby
type: docs
weight: 50
url: /sv/java/remove-all-macros-from-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Ta bort alla makron från Visio Diagram**
 För att ta bort alla makron från Visio Diagram med**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**Ta bort alla makron från diagrammet** modul. Här kan du se exempelkod.

**Ruby kod**

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
## **Ladda ner Running Code**
 Ladda ner**Ta bort alla makron från Visio Diagram (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/removeallmacrosfromdiagram.rb)
