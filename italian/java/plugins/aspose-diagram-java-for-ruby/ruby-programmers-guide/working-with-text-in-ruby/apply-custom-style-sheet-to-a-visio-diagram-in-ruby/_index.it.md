---
title: Applica foglio di stile personalizzato a Visio Diagram in Ruby
type: docs
weight: 10
url: /it/java/apply-custom-style-sheet-to-a-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Applica foglio di stile personalizzato a un Visio Diagram**
 Per applicare un foglio di stile personalizzato a un Visio Diagram utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**Applica foglio di stile personalizzato** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 dati_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/dati/'

\# Crea un'istanza di Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

forme = diagram.getPages().getPage(0).getShapes()

io = 0

 mentre io< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process"

        source_shape = shape

        break

    end

    i +=1

end

\# Find the required style sheet

stylesheets = diagram.getStyleSheets()

j = 0

while j < stylesheets.getCount()

    stylesheet = stylesheets.get(j)

    if stylesheet.getName() == "Basic"

        custom_stylesheet = stylesheet

        break

    end

    j +=1

end

if source_shape != nil && custom_stylesheet != nil

    # Apply text style

    source_shape.setTextStyle(custom_stylesheet)

    # Apply fill style

    source_shape.setFillStyle(custom_stylesheet)

    # Apply line style

    source_shape.setLineStyle(custom_stylesheet)

end

\# Save diagram

diagram.save(data_dir + "ApplyCustomStyleSheet.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Applied custom stylesheet to a visio diagram."

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Applica foglio di stile personalizzato a un Visio Diagram (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Text/applycustomstylesheet.rb)
