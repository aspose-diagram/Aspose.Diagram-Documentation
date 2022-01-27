---
title: Retrieve Drawing Font Information in Ruby
type: docs
weight: 30
url: /java/retrieve-drawing-font-information-in-ruby/
---

## **Aspose.Diagram - Retrieve Drawing Font Information**
To Retrieve Drawing Font Information using **Aspose.Diagram Java for Ruby**, simply invoke **GetDiagramFontInfo** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

fonts = diagram.getFonts()

i = 0

while i < fonts.getCount()

    font = fonts.get(i)

    # Display information about the fonts

    puts font.getName()

    i +=1

end

{{< /highlight >}}
## **Download Running Code**
Download **Retrieve Drawing Font Information (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/getdiagramfontinfo.rb)
