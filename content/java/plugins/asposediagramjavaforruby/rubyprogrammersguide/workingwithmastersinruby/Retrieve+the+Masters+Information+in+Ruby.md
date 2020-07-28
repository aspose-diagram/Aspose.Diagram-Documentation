+++
title = "Retrieve the Masters Information in Ruby" 
description = "" 
weight = 20108 
+++

Aspose.Diagram for Java : Retrieve the Masters Information in Ruby  

# Aspose.Diagram for Java : Retrieve the Masters Information in Ruby


## Aspose.Diagram - Retrieve the Masters Information

To Retrieve the Masters Information using **Aspose.Diagram Java for Ruby**, simply invoke **GetMasterInfo** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Call the diagram constructor to load diagram from a VSD filediagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")masters = diagram.getMasters()i = 0while i < masters.getCount()    master = masters.get(i)    puts "Master ID : " + master.getID().to\_s    puts "Master Name : " + master.getName().to\_s    i +=1end

## Download Running Code

Download **Retrieve the Masters Information (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/getmasterinfo.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Masters/getmasterinfo.rb)

