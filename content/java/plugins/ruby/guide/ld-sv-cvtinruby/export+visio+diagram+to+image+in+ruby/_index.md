---
title : "Export Visio Diagram to Image in Ruby" 
description : "" 
weight : 20097 
toc : false
type: docs
url: /java/plugins/ruby/guide/ld-sv-cvtinruby/export+visio+diagram+to+image+in+ruby/
---

# Aspose.Diagram for Java : Export Visio Diagram to Image in Ruby


## Aspose.Diagram - Export Visio Diagram to Image

To Export Visio Diagram to Image using **Aspose.Diagram Java for Ruby**, simply invoke **ExportToImage** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Call the diagram constructor to load diagram from a VSD filediagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")# Save as PNGdiagram.save(data\_dir + "Diagram.png", Rjb::import('com.aspose.diagram.SaveFileFormat').PNG)puts "Exported visio diagram to PNG."

## Download Running Code

Download **Export Visio Diagram to Image (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoimage.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Export/exporttoimage.rb)

