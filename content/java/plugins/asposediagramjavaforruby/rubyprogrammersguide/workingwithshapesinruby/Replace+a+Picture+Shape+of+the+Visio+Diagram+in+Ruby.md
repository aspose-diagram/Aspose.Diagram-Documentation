+++
title = "Replace a Picture Shape of the Visio Diagram in Ruby" 
description = "" 
weight = 20125 
+++

Aspose.Diagram for Java : Replace a Picture Shape of the Visio Diagram in Ruby  

# Aspose.Diagram for Java : Replace a Picture Shape of the Visio Diagram in Ruby


## Aspose.Diagram - Replace a Picture Shape of the Visio Diagram

To Replace a Picture Shape of the Visio Diagram using **Aspose.Diagram Java for Ruby**, simply invoke **ReplacePictureShape** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")# convert image into bytes arrayfi = Rjb::import('java.io.File').new(data\_dir + "star.png")file\_content = Rjb::import('java.nio.file.Files').readAllBytes(fi.toPath())shapes = diagram.getPages().getPage("Flow 1").getShapes()i = 0while i < shapes.getCount()    shape = shapes.get(i)    # Filter shapes by type Foreign    if shape.getType() == Rjb::import('com.aspose.diagram.TypeValue').FOREIGN        # replace picture shape        shape.getForeignData().setValue(file\_content)    end    i +=1end# Save diagramdiagram.save(data\_dir + "ReplacePictureShape.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Replaced picture shape successfully!"

## Download Running Code

Download **Replace a Picture Shape of the Visio Diagram (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/replacepictureshape.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Shapes/replacepictureshape.rb)

