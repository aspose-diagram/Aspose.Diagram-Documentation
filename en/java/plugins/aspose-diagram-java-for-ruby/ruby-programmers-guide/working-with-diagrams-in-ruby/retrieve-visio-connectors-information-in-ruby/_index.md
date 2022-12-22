---
title: Retrieve Visio Connectors Information in Ruby
type: docs
weight: 20
url: /java/retrieve-visio-connectors-information-in-ruby/
---

## **Aspose.Diagram - Retrieve Visio Connectors Information**
To Retrieve Visio Connectors Information using **Aspose.Diagram Java for Ruby**, simply invoke **GetConnectorsInfo** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

connectors = diagram.getPages().getPage(0).getConnects()

i = 0

while i < connectors.getCount()

    connector = connectors.get(i)

    # Display information about the Connectors

    puts "From Shape ID : " + connector.getFromSheet().to_s

    puts "To Shape ID : " + connector.getToSheet().to_s

    i +=1

end

{{< /highlight >}}
## **Download Running Code**
Download **Retrieve Visio Connectors Information (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/getconnectorsinfo.rb)

