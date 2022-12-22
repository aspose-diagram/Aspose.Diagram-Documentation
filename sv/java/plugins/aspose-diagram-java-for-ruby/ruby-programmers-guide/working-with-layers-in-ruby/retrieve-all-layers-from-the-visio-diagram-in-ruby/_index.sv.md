---
title: Hämta alla lager från Visio Diagram i Ruby
type: docs
weight: 30
url: /sv/java/retrieve-all-layers-from-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Hämta alla lager**
 För att hämta alla lager med hjälp av**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**GetAllLayers** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FIL__)))) + '/data/'

\# Skapa instans av Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# få Visio sida

sida = diagram.getPages().getPage(0)

lager = page.getPageSheet().getLayers()

i = 0

 medan jag< layers.getCount()

    layer = layers.get(i)

    puts "Name: " + layer.getName().getValue().to_s

    puts "Visibility: " + layer.getVisible().getValue().to_s

    puts "Status: " + layer.getStatus().getValue().to_s



    i +=1

end

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Hämta alla lager från Visio Diagram (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Layers/getalllayers.rb)
