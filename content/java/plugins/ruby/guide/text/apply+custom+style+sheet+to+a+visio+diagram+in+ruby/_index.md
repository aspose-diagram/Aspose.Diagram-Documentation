---
title : "Apply Custom Style Sheet to a Visio Diagram in Ruby" 
description : "" 
weight : 20136 
toc : false
type: docs
url: /java/plugins/ruby/guide/text/apply+custom+style+sheet+to+a+visio+diagram+in+ruby/
---

# Aspose.Diagram for Java : Apply Custom Style Sheet to a Visio Diagram in Ruby


## Aspose.Diagram - Apply Custom Style Sheet to a Visio Diagram

To Apply Custom Style Sheet to a Visio Diagram using **Aspose.Diagram Java for Ruby**, simply invoke **ApplyCustomStyleSheet** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")shapes = diagram.getPages().getPage(0).getShapes()i = 0while i < shapes.getCount()    shape = shapes.get(i)    if shape.getNameU() == "Process"        source\_shape = shape        break    end    i +=1end# Find the required style sheetstylesheets = diagram.getStyleSheets()j = 0while j < stylesheets.getCount()    stylesheet = stylesheets.get(j)    if stylesheet.getName() == "Basic"        custom\_stylesheet = stylesheet        break    end    j +=1endif source\_shape != nil && custom\_stylesheet != nil    # Apply text style    source\_shape.setTextStyle(custom\_stylesheet)    # Apply fill style    source\_shape.setFillStyle(custom\_stylesheet)    # Apply line style    source\_shape.setLineStyle(custom\_stylesheet)end# Save diagramdiagram.save(data\_dir + "ApplyCustomStyleSheet.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Applied custom stylesheet to a visio diagram."

## Download Running Code

Download **Apply Custom Style Sheet to a Visio Diagram (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Text/applycustomstylesheet.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Text/applycustomstylesheet.rb)

