---
title: Create an empty Visio Diagram in Ruby
type: docs
weight: 10
url: /java/create-an-empty-visio-diagram-in-ruby/
---

## **Aspose.Diagram - Create an empty Visio Diagram**
To Create an empty Visio Diagram using **Aspose.Diagram Java for Ruby**, simply invoke **CreateDiagram** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new

\# Save as VDX

diagram.save(data_dir + "CreateDiagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Created visio diagram successfully!"

{{< /highlight >}}
## **Download Running Code**
Download **Create an empty Visio Diagram (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/creatediagram.rb)
