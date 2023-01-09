---
title: Hämta information om ritningsteckensnitt i Ruby
type: docs
weight: 30
url: /sv/java/retrieve-drawing-font-information-in-ruby/
---
## **Aspose.Diagram - Hämta information om ritningsteckensnitt**
 För att hämta information om ritningsteckensnitt med hjälp av**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**GetDiagramFontInfo** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FIL__)))) + '/data/'

\# Skapa instans av Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

teckensnitt = diagram.getFonts()

i = 0

 medan jag< fonts.getCount()

    font = fonts.get(i)

    # Display information about the fonts

    puts font.getName()

    i +=1

end

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Hämta information om ritningsteckensnitt (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/getdiagramfontinfo.rb)
