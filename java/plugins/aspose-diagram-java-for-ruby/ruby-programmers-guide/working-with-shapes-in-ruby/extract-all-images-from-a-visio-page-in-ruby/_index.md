---
title: Extract All Images From a Visio Page in Ruby
type: docs
weight: 30
url: /java/extract-all-images-from-a-visio-page-in-ruby/
---

## **Aspose.Diagram - Extract All Images From a Visio Page**
To Extract All Images From a Visio Page using **Aspose.Diagram Java for Ruby**, simply invoke **ExtractImages** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

shapes = diagram.getPages().getPage("Flow 1").getShapes()

i = 0

while i < shapes.getCount()

    shape = shapes.get(i)

    # Filter shapes by type Foreign

    if shape.getType() == Rjb::import('com.aspose.diagram.TypeValue').FOREIGN

        # create an image file

        fos = Rjb::import('java.io.FileOutputStream').new(data_dir + "Image#{i}.bmp")

        fos.write(shape.getForeignData().getValue())

        fos.close()

    end

    i +=1

end

puts "Extracted images successfully!"

{{< /highlight >}}
## **Download Running Code**
Download **Extract All Images From a Visio Page (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/extractimages.rb)
