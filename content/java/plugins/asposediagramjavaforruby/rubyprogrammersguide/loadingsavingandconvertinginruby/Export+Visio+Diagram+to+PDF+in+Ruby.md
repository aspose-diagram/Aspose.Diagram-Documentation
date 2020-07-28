+++
title = "Export Visio Diagram to PDF in Ruby" 
description = "" 
weight = 20098 
+++

Aspose.Diagram for Java : Export Visio Diagram to PDF in Ruby  

# Aspose.Diagram for Java : Export Visio Diagram to PDF in Ruby


## Aspose.Diagram - Export Visio Diagram to PDF

To Export Visio Diagram to PDF using **Aspose.Diagram Java for Ruby**, simply invoke **ExportToPdf** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Call the diagram constructor to load diagram from a VSD filediagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")# Save as PDF file formatdiagram.save(data\_dir + "Diagram.pdf", Rjb::import('com.aspose.diagram.SaveFileFormat').PDF)puts "Exported visio diagram to pdf."

## Download Running Code

Download **Export Visio Diagram to PDF (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttopdf.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Export/exporttopdf.rb)

