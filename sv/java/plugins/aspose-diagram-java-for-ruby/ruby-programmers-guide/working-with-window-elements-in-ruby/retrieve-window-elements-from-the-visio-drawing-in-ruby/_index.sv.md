---
title: Hämta fönsterelement från Visio-ritningen i rubin
type: docs
weight: 30
url: /sv/java/retrieve-window-elements-from-the-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Hämta fönsterelement från Visio-ritningen**
 För att hämta fönsterelement från Visio-ritningen med hjälp av**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**GetWindowElements** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FIL__)))) + '/data/'

\# Skapa instans av Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

windows = diagram.getWindows()

i = 0

 medan jag< windows.getCount()

    window = windows.get(i)

    puts "ID: " + window.getID().to_s

    puts "Type: " + window.getWindowType().to_s

    puts "Window height: " + window.getWindowHeight().to_s

    puts "Window width: " + window.getWindowWidth().to_s

    puts "Window state: " + window.getWindowState().to_s

    i +=1

end

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Hämta fönsterelement från Visio-ritningen (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/getwindowelements.rb)
