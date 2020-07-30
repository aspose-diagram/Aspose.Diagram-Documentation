---
title : "Retrieve Visio Connectors Information in Ruby" 
description : "" 
weight : 20111 
toc : false
type: docs
url: /java/plugins/ruby/guide/diagrams/retrieve+visio+connectors+information+in+ruby/
---

# Aspose.Diagram for Java : Retrieve Visio Connectors Information in Ruby


## Aspose.Diagram - Retrieve Visio Connectors Information

To Retrieve Visio Connectors Information using **Aspose.Diagram Java for Ruby**, simply invoke **GetConnectorsInfo** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")connectors = diagram.getPages().getPage(0).getConnects()i = 0while i < connectors.getCount()    connector = connectors.get(i)    # Display information about the Connectors    puts "From Shape ID : " + connector.getFromSheet().to\_s    puts "To Shape ID : " + connector.getToSheet().to\_s    i +=1end

## Download Running Code

Download **Retrieve Visio Connectors Information (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/getconnectorsinfo.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Diagrams/getconnectorsinfo.rb)

