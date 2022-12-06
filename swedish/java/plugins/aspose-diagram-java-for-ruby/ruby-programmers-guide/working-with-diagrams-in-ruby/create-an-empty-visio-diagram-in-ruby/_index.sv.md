---
title: Skapa ett tomt Visio Diagram i Ruby
type: docs
weight: 10
url: /sv/java/create-an-empty-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Skapa en tom Visio Diagram**
 För att skapa en tom Visio Diagram med hjälp av**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**Skapa Diagram** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new

\# Save as VDX

diagram.save(data_dir + "CreateDiagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Created visio diagram successfully!"

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Skapa ett tomt Visio Diagram (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/creatediagram.rb)
