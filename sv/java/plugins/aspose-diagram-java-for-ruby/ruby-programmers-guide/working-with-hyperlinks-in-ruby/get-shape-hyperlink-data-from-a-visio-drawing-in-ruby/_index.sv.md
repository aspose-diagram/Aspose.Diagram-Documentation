---
title: Få Shape Hyperlink Data från en Visio-ritning i Ruby
type: docs
weight: 20
url: /sv/java/get-shape-hyperlink-data-from-a-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Hämta Shape Hyperlink Data**
För att få Shape Hyperlink Data med hjälp av**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**GetShapeHyperlinkData** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FIL__)))) + '/data/'

\# Skapa instans av Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Hyperlinks.vdx")

\# Få en viss form

shape = diagram.getPages().getPage("Flöde 1").getShapes().getShape(1)

hyperlänkar = shape.getHyperlinks()

i = 0

 medan jag< hyperlinks.getCount()

    hyperlink = hyperlinks.get(i)

    puts "Address: " + hyperlink.getAddress().getValue().to_s

    puts "Sub Address: " + hyperlink.getSubAddress().getValue().to_s

    puts "Description: " + hyperlink.getDescription().getValue().to_s

    i +=1

end

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Hämta Shape-hyperlänkdata från en Visio-ritning (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Hyperlinks/getshapehyperlinkdata.rb)
