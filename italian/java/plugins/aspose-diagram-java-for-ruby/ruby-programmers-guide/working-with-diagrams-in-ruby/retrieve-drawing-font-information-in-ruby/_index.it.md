---
title: Recupera le informazioni sui caratteri del disegno in Ruby
type: docs
weight: 30
url: /it/java/retrieve-drawing-font-information-in-ruby/
---
## **Aspose.Diagram - Recupera informazioni sui caratteri del disegno**
 Per recuperare le informazioni sui caratteri del disegno utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**OttieniDiagramFontInfo** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 dati_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/dati/'

\# Crea un'istanza di Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

caratteri = diagram.getFonts()

io = 0

 mentre io< fonts.getCount()

    font = fonts.get(i)

    # Display information about the fonts

    puts font.getName()

    i +=1

end

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Recupera informazioni sui caratteri del disegno (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/getdiagramfontinfo.rb)
