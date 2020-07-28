+++
title = "Retrieve Window Elements from the Visio Drawing in Ruby" 
description = "" 
weight = 20142 
+++

Aspose.Diagram for Java : Retrieve Window Elements from the Visio Drawing in Ruby  

# Aspose.Diagram for Java : Retrieve Window Elements from the Visio Drawing in Ruby


## Aspose.Diagram - Retrieve Window Elements from the Visio Drawing

To Retrieve Window Elements from the Visio Drawing using **Aspose.Diagram Java for Ruby**, simply invoke **GetWindowElements** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")windows = diagram.getWindows()i = 0while i < windows.getCount()    window = windows.get(i)    puts "ID: " + window.getID().to\_s    puts "Type: " + window.getWindowType().to\_s    puts "Window height: " + window.getWindowHeight().to\_s    puts "Window width: " + window.getWindowWidth().to\_s    puts "Window state: " + window.getWindowState().to\_s    i +=1end

## Download Running Code

Download **Retrieve Window Elements from the Visio Drawing (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/getwindowelements.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/WindowElements/getwindowelements.rb)

