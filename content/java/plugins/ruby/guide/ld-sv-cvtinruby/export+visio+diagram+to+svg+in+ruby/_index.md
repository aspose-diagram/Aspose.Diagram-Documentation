---
title : "Export Visio Diagram to SVG in Ruby" 
description : "" 
weight : 20099 
toc : false
type: docs
url: /java/plugins/ruby/guide/ld-sv-cvtinruby/export+visio+diagram+to+svg+in+ruby/
---

# Aspose.Diagram for Java : Export Visio Diagram to SVG in Ruby


## Aspose.Diagram - Export Visio Diagram to SVG

To Export Visio Diagram to SVG using **Aspose.Diagram Java for Ruby**, simply invoke **ExportToSvg** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Call the diagram constructor to load diagram from a VSD filediagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")# Save as SVGdiagram.save(data\_dir + "Diagram.svg", Rjb::import('com.aspose.diagram.SaveFileFormat').SVG)puts "Exported visio diagram to SVG."

## Download Running Code

Download **Export Visio Diagram to SVG (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttosvg.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Export/exporttosvg.rb)

