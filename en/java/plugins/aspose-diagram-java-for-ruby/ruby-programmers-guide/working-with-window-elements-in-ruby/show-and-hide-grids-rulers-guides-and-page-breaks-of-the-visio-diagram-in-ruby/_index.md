---
title: Show and Hide Grids, Rulers, Guides and Page Breaks of the Visio Diagram in Ruby
type: docs
weight: 40
url: /java/show-and-hide-grids-rulers-guides-and-page-breaks-of-the-visio-diagram-in-ruby/
---

## **Aspose.Diagram - Show and Hide Grids, Rulers, Guides and Page Breaks of the Visio Diagram**
To Show and Hide Grids, Rulers, Guides and Page Breaks of the Visio Diagram using **Aspose.Diagram Java for Ruby**, simply invoke **ShowHideProperties** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# get window object by index

window = diagram.getWindows().get(0)

\# set visibility of grid

window.setShowGrid(1)

\# set visibility of guides

window.setShowGuides(1)

\# set visibility of rulers

window.setShowRulers(1)

\# set visibility of page breaks

window.setShowPageBreaks(1)

\# save in any supported format

diagram.save(data_dir + "ShowHideProperties.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Show and Hide Grids, Rulers, Guides and Page Breaks of the Visio Diagram."

{{< /highlight >}}
## **Download Running Code**
Download **Show and Hide Grids, Rulers, Guides and Page Breaks of the Visio Diagram (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/showhideproperties.rb)
