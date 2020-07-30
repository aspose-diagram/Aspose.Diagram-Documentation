---
title : "Retrieve Drawing Font Information in Ruby" 
description : "" 
weight : 20112 
toc : false
type: docs
url: /java/plugins/ruby/guide/diagrams/retrieve+drawing+font+information+in+ruby/
---

# Aspose.Diagram for Java : Retrieve Drawing Font Information in Ruby


## Aspose.Diagram - Retrieve Drawing Font Information

To Retrieve Drawing Font Information using **Aspose.Diagram Java for Ruby**, simply invoke **GetDiagramFontInfo** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")fonts = diagram.getFonts()i = 0while i < fonts.getCount()    font = fonts.get(i)    # Display information about the fonts    puts font.getName()    i +=1end

## Download Running Code

Download **Retrieve Drawing Font Information (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/getdiagramfontinfo.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Diagrams/getdiagramfontinfo.rb)

