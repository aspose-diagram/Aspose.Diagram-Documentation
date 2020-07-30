---
title : "Add Hyperlink to a Visio Shape in Ruby" 
description : "" 
weight : 20154 
toc : false
type: docs
url: /java/plugins/ruby/guide/hyperlinks/add+hyperlink+to+a+visio+shape+in+ruby/
---

# Aspose.Diagram for Java : Add Hyperlink to a Visio Shape in Ruby


## Aspose.Diagram - Add Hyperlink

To Add Hyperlink using **Aspose.Diagram Java for Ruby**, simply invoke **AddHyperlinkToShape** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")# Initialize Hyperlink objecthyperlink = Rjb::import('com.aspose.diagram.Hyperlink').new# Set address valuehyperlink.getAddress().setValue("http://www.google.com/")# Set sub address valuehyperlink.getSubAddress().setValue("Sub address here")# Set description valuehyperlink.getDescription().setValue("Description here")# Set namehyperlink.setName("MyHyperLink")# Add hyperlink to the shapediagram.getPages().getPage("Flow 1").getShapes().getShape(1).getHyperlinks().add(hyperlink)# Save diagramdiagram.save(data\_dir + "Hyperlinks.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Added hyperlik to shape successfully!"

## Download Running Code

Download **Add Hyperlink to a Visio Shape (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Hyperlinks/addhyperlinktoshape.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Hyperlinks/addhyperlinktoshape.rb)

