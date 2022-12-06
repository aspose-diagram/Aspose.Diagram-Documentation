---
title: Export Visio Diagram to Image in Ruby
type: docs
weight: 30
url: /java/export-visio-diagram-to-image-in-ruby/
---

## **Aspose.Diagram - Export Visio Diagram to Image**
To Export Visio Diagram to Image using **Aspose.Diagram Java for Ruby**, simply invoke **ExportToImage** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as PNG

diagram.save(data_dir + "Diagram.png", Rjb::import('com.aspose.diagram.SaveFileFormat').PNG)

puts "Exported visio diagram to PNG."

{{< /highlight >}}
## **Download Running Code**
Download **Export Visio Diagram to Image (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoimage.rb)
