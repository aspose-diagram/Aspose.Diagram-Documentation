---
title: Get Shape Hyperlink Data from a Visio Drawing in Ruby
type: docs
weight: 20
url: /java/get-shape-hyperlink-data-from-a-visio-drawing-in-ruby/
---

## **Aspose.Diagram - Get Shape Hyperlink Data**
To Get Shape Hyperlink Data using **Aspose.Diagram Java for Ruby**, simply invoke **GetShapeHyperlinkData** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Hyperlinks.vdx")

\# Get a particular shape

shape = diagram.getPages().getPage("Flow 1").getShapes().getShape(1)

hyperlinks = shape.getHyperlinks()

i = 0

while i < hyperlinks.getCount()

    hyperlink = hyperlinks.get(i)

    puts "Address: " + hyperlink.getAddress().getValue().to_s

    puts "Sub Address: " + hyperlink.getSubAddress().getValue().to_s

    puts "Description: " + hyperlink.getDescription().getValue().to_s

    i +=1

end

{{< /highlight >}}
## **Download Running Code**
Download **Get Shape Hyperlink Data from a Visio Drawing (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Hyperlinks/getshapehyperlinkdata.rb)
- [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Hyperlinks/getshapehyperlinkdata.rb)
