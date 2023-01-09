---
title: Estrai tutte le immagini da una pagina Visio in Ruby
type: docs
weight: 30
url: /it/java/extract-all-images-from-a-visio-page-in-ruby/
---
## **Aspose.Diagram - Estrai tutte le immagini da una pagina Visio**
 Per estrarre tutte le immagini da una pagina Visio utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**Estrai immagini** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 dati_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/dati/'

\# Crea un'istanza di Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

forme = diagram.getPages().getPage("Flusso 1").getShapes()

io = 0

 mentre io< shapes.getCount()

    shape = shapes.get(i)

    # Filter shapes by type Foreign

    if shape.getType() == Rjb::import('com.aspose.diagram.TypeValue').FOREIGN

        # create an image file

        fos = Rjb::import('java.io.FileOutputStream').new(data_dir + "Image#{i}.bmp")

        fos.write(shape.getForeignData().getValue())

        fos.close()

    end

    i +=1

end

puts "Extracted images successfully!"

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Estrai tutte le immagini da una pagina Visio (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/extractimages.rb)
