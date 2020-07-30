---
title : "Manage Headers and Footers of the Visio Diagrams in Ruby" 
description : "" 
weight : 20148 
toc : false
type: docs
url: /java/plugins/ruby/guide/headersandfooters/manage+headers+and+footers+of+the+visio+diagrams+in+ruby/
---

# Aspose.Diagram for Java : Manage Headers and Footers of the Visio Diagrams in Ruby


## Aspose.Diagram - Manage Headers and Footers of the Visio Diagrams

To Manage Headers and Footers of the Visio Diagrams using **Aspose.Diagram Java for Ruby**, simply invoke **HeadersAndFooters** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")# add page number at the right corner of headerdiagram.getHeaderFooter().setHeaderRight("&p")# set text at the centerdiagram.getHeaderFooter().setHeaderCenter("Center of the header")# set text at the left sidediagram.getHeaderFooter().setHeaderLeft("Left of the header")# add text at the right corner of footerdiagram.getHeaderFooter().setFooterRight("Right of the footer")# set text at the centerdiagram.getHeaderFooter().setFooterCenter("Center of the footer")# set text at the left sidediagram.getHeaderFooter().setFooterLeft("Left of the footer")# set header & footer colordiagram.getHeaderFooter().setHeaderFooterColor(Rjb::import('com.aspose.diagram.Color').getRed())# set text font propertiesdiagram.getHeaderFooter().getHeaderFooterFont().setItalic(1)diagram.getHeaderFooter().getHeaderFooterFont().setUnderline(0)# Save diagramdiagram.save(data\_dir + "HeadersAndFooters.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Done with headers and footers."

## Download Running Code

Download **Manage Headers and Footers of the Visio Diagrams (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/HeadersAndFooters/headersandfooters.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/HeadersAndFooters/headersandfooters.rb)

