---
title: Hämta Visio Anslutningsinformation i Ruby
type: docs
weight: 20
url: /sv/java/retrieve-visio-connectors-information-in-ruby/
---
## **Aspose.Diagram - Hämta Visio Anslutningsinformation**
 För att hämta Visio Anslutningsinformation med hjälp av**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**GetConnectorsInfo** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FIL__)))) + '/data/'

\# Skapa instans av Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

connectors = diagram.getPages().getPage(0).getConnects()

i = 0

 medan jag< connectors.getCount()

    connector = connectors.get(i)

    # Display information about the Connectors

    puts "From Shape ID : " + connector.getFromSheet().to_s

    puts "To Shape ID : " + connector.getToSheet().to_s

    i +=1

end

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Hämta Visio Anslutningsinformation (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/getconnectorsinfo.rb)

