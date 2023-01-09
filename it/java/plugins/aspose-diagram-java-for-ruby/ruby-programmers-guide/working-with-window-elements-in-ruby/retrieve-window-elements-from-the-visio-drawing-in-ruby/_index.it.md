---
title: Recupera gli elementi della finestra dal disegno Visio in Ruby
type: docs
weight: 30
url: /it/java/retrieve-window-elements-from-the-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Recupera elementi finestra dal disegno Visio**
 Per recuperare gli elementi della finestra dal disegno Visio utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**GetWindowElements** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 dati_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/dati/'

\# Crea un'istanza di Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

finestre = diagram.getWindows()

io = 0

 mentre io< windows.getCount()

    window = windows.get(i)

    puts "ID: " + window.getID().to_s

    puts "Type: " + window.getWindowType().to_s

    puts "Window height: " + window.getWindowHeight().to_s

    puts "Window width: " + window.getWindowWidth().to_s

    puts "Window state: " + window.getWindowState().to_s

    i +=1

end

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Recupera elementi finestra dal disegno Visio (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/getwindowelements.rb)
