---
title: Retrieve the Masters Information in Ruby
type: docs
weight: 30
url: /java/retrieve-the-masters-information-in-ruby/
---

## **Aspose.Diagram - Retrieve the Masters Information**
To Retrieve the Masters Information using **Aspose.Diagram Java for Ruby**, simply invoke **GetMasterInfo** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

masters = diagram.getMasters()

i = 0

while i < masters.getCount()

    master = masters.get(i)

    puts "Master ID : " + master.getID().to_s

    puts "Master Name : " + master.getName().to_s

    i +=1

end

{{< /highlight >}}
## **Download Running Code**
Download **Retrieve the Masters Information (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/getmasterinfo.rb)
- [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Masters/getmasterinfo.rb)
