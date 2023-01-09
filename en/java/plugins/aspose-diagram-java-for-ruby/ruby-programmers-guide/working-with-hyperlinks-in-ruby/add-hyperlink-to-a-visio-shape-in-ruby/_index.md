---
title: Add Hyperlink to a Visio Shape in Ruby
type: docs
weight: 10
url: /java/add-hyperlink-to-a-visio-shape-in-ruby/
---

## **Aspose.Diagram - Add Hyperlink**
To Add Hyperlink using **Aspose.Diagram Java for Ruby**, simply invoke **AddHyperlinkToShape** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Initialize Hyperlink object

hyperlink = Rjb::import('com.aspose.diagram.Hyperlink').new

\# Set address value

hyperlink.getAddress().setValue("http://www.google.com/")

\# Set sub address value

hyperlink.getSubAddress().setValue("Sub address here")

\# Set description value

hyperlink.getDescription().setValue("Description here")

\# Set name

hyperlink.setName("MyHyperLink")

\# Add hyperlink to the shape

diagram.getPages().getPage("Flow 1").getShapes().getShape(1).getHyperlinks().add(hyperlink)

\# Save diagram

diagram.save(data_dir + "Hyperlinks.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Added hyperlik to shape successfully!"

{{< /highlight >}}
## **Download Running Code**
Download **Add Hyperlink to a Visio Shape (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Hyperlinks/addhyperlinktoshape.rb)
