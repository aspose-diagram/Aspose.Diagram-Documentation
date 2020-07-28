+++
title = "Apply Different Style on the Each Text Value of a Shape in Ruby" 
description = "" 
weight = 20137 
+++

Aspose.Diagram for Java : Apply Different Style on the Each Text Value of a Shape in Ruby  

# Aspose.Diagram for Java : Apply Different Style on the Each Text Value of a Shape in Ruby


## Aspose.Diagram - Apply Different Style on the Each Text Value of a Shape

To Apply Different Style on the Each Text Value of a Shape using **Aspose.Diagram Java for Ruby**, simply invoke **AddShapeTextAndStyles** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")# Get a particular shapeshape = diagram.getPages().getPage("Flow 1").getShapes().getShape(1)# Clear shape text values and charsshape.getText().getValue().clear()shape.getChars().clear()# Mark character run and add textshape.getText().getValue().add(Rjb::import('com.aspose.diagram.Cp').new(0))shape.getText().getValue().add(Rjb::import('com.aspose.diagram.Txt').new("TextStyle\_Regular"))shape.getText().getValue().add(Rjb::import('com.aspose.diagram.Cp').new(1))shape.getText().getValue().add(Rjb::import('com.aspose.diagram.Txt').new("TextStyle\_Bold\_Italic"))shape.getText().getValue().add(Rjb::import('com.aspose.diagram.Cp').new(2))shape.getText().getValue().add(Rjb::import('com.aspose.diagram.Txt').new("TextStyle\_Underline\_Italic"))shape.getText().getValue().add(Rjb::import('com.aspose.diagram.Cp').new(3))shape.getText().getValue().add(Rjb::import('com.aspose.diagram.Txt').new("TextStyle\_Bold\_Italic\_Underline"))# Add formatting charactersshape.getChars().add(Rjb::import('com.aspose.diagram.Char').new)shape.getChars().add(Rjb::import('com.aspose.diagram.Char').new)shape.getChars().add(Rjb::import('com.aspose.diagram.Char').new)shape.getChars().add(Rjb::import('com.aspose.diagram.Char').new)style\_value = Rjb::import('com.aspose.diagram.StyleValue')# Set properties e.g. color, font, size and style etc.shape.getChars().getChar(0).setIX(0)shape.getChars().getChar(0).getColor().setValue("#FF0000")shape.getChars().getChar(0).getFont().setValue(4)shape.getChars().getChar(0).getSize().setValue(0.22)shape.getChars().getChar(0).getStyle().setValue(style\_value.UNDEFINED)# Set properties e.g. color, font, size and style etc.shape.getChars().getChar(1).setIX(1)shape.getChars().getChar(1).getColor().setValue("#FF00FF")shape.getChars().getChar(1).getFont().setValue(4)shape.getChars().getChar(1).getSize().setValue(0.22)shape.getChars().getChar(1).getStyle().setValue(style\_value.BOLD | style\_value.ITALIC)# Set properties e.g. color, font, size and style etc.shape.getChars().getChar(2).setIX(2)shape.getChars().getChar(2).getColor().setValue("#00FF00")shape.getChars().getChar(2).getFont().setValue(4)shape.getChars().getChar(2).getSize().setValue(0.22)shape.getChars().getChar(2).getStyle().setValue(style\_value.UNDERLINE | style\_value.ITALIC)# Save diagramdiagram.save(data\_dir + "AddShapeTextAndStyles.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Added shape text and styles."

## Download Running Code

Download **Apply Different Style on the Each Text Value of a Shape (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Text/addshapetextandstyles.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Text/addshapetextandstyles.rb)

