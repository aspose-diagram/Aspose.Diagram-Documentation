---
title: Retrieve All Layers from the Visio Diagram in Ruby
type: docs
weight: 30
url: /java/retrieve-all-layers-from-the-visio-diagram-in-ruby/
---

## **Aspose.Diagram - Retrieve All Layers**
To Retrieve All Layers using **Aspose.Diagram Java for Ruby**, simply invoke **GetAllLayers** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# get Visio page

page = diagram.getPages().getPage(0)

layers = page.getPageSheet().getLayers()

i = 0

while i < layers.getCount()

    layer = layers.get(i)

    puts "Name: " + layer.getName().getValue().to_s

    puts "Visibility: " + layer.getVisible().getValue().to_s

    puts "Status: " + layer.getStatus().getValue().to_s



    i +=1

end

{{< /highlight >}}
## **Download Running Code**
Download **Retrieve All Layers from the Visio Diagram (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Layers/getalllayers.rb)
- [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Layers/getalllayers.rb)
