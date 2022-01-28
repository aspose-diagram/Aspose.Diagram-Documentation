---
title: Apply Custom Style Sheet to a Visio Diagram in Ruby
type: docs
weight: 10
url: /java/apply-custom-style-sheet-to-a-visio-diagram-in-ruby/
---

## **Aspose.Diagram - Apply Custom Style Sheet to a Visio Diagram**
To Apply Custom Style Sheet to a Visio Diagram using **Aspose.Diagram Java for Ruby**, simply invoke **ApplyCustomStyleSheet** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

shapes = diagram.getPages().getPage(0).getShapes()

i = 0

while i < shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process"

        source_shape = shape

        break

    end

    i +=1

end

\# Find the required style sheet

stylesheets = diagram.getStyleSheets()

j = 0

while j < stylesheets.getCount()

    stylesheet = stylesheets.get(j)

    if stylesheet.getName() == "Basic"

        custom_stylesheet = stylesheet

        break

    end

    j +=1

end

if source_shape != nil && custom_stylesheet != nil

    # Apply text style

    source_shape.setTextStyle(custom_stylesheet)

    # Apply fill style

    source_shape.setFillStyle(custom_stylesheet)

    # Apply line style

    source_shape.setLineStyle(custom_stylesheet)

end

\# Save diagram

diagram.save(data_dir + "ApplyCustomStyleSheet.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Applied custom stylesheet to a visio diagram."

{{< /highlight >}}
## **Download Running Code**
Download **Apply Custom Style Sheet to a Visio Diagram (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Text/applycustomstylesheet.rb)
