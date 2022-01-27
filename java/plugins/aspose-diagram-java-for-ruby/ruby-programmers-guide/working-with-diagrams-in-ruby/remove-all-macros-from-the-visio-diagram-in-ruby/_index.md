---
title: Remove All Macros from the Visio Diagram in Ruby
type: docs
weight: 50
url: /java/remove-all-macros-from-the-visio-diagram-in-ruby/
---

## **Aspose.Diagram - Remove All Macros from the Visio Diagram**
To Remove All Macros from the Visio Diagram using **Aspose.Diagram Java for Ruby**, simply invoke **RemoveAllMacrosFromDiagram** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# remove all macros

diagram.setVbProjectData(nil)

\# Save as VDX

diagram.save(data_dir + "RemoveAllMacros.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Removed all macros from diagram successfully!"

{{< /highlight >}}
## **Download Running Code**
Download **Remove All Macros from the Visio Diagram (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/removeallmacrosfromdiagram.rb)
