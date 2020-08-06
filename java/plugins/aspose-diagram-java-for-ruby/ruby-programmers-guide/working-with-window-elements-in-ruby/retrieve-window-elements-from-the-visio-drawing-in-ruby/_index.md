---
title: Retrieve Window Elements from the Visio Drawing in Ruby
type: docs
weight: 30
url: /java/retrieve-window-elements-from-the-visio-drawing-in-ruby/
---

## **Aspose.Diagram - Retrieve Window Elements from the Visio Drawing**
To Retrieve Window Elements from the Visio Drawing using **Aspose.Diagram Java for Ruby**, simply invoke **GetWindowElements** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

windows = diagram.getWindows()

i = 0

while i < windows.getCount()

    window = windows.get(i)

    puts "ID: " + window.getID().to_s

    puts "Type: " + window.getWindowType().to_s

    puts "Window height: " + window.getWindowHeight().to_s

    puts "Window width: " + window.getWindowWidth().to_s

    puts "Window state: " + window.getWindowState().to_s

    i +=1

end

{{< /highlight >}}
## **Download Running Code**
Download **Retrieve Window Elements from the Visio Drawing (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/getwindowelements.rb)
- [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/WindowElements/getwindowelements.rb)
