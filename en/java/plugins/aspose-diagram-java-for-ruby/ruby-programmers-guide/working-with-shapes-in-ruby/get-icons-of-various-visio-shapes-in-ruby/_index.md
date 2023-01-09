---
title: Get Icons of Various Visio Shapes in Ruby
type: docs
weight: 40
url: /java/get-icons-of-various-visio-shapes-in-ruby/
---

## **Aspose.Diagram - Get Icons of Various Visio Shapes**
To Get Icons of Various Visio Shapes using **Aspose.Diagram Java for Ruby**, simply invoke **GetShapeIcon** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Basic_Shapes.vsd")

\# get master

master = diagram.getMasters().getMasterByName("Circle")

\# get byte array

bytes = master.getIcon()

\# create an image file

fos = Rjb::import('java.io.FileOutputStream').new(data_dir + "MyImage.png")

\# write byte array of the image

fos.write(bytes)

\# close array

fos.close()

puts "Get shape icon, please check the output file."

{{< /highlight >}}
## **Download Running Code**
Download **Get Icons of Various Visio Shapes (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/getshapeicon.rb)
