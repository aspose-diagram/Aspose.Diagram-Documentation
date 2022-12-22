---
title: Sostituisci una forma immagine di Visio Diagram in Ruby
type: docs
weight: 60
url: /it/java/replace-a-picture-shape-of-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Sostituisci una forma immagine del Visio Diagram**
 Per sostituire una forma immagine del Visio Diagram utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**SostituisciPictureShape** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 dati_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/dati/'

\# Crea un'istanza di Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# converte l'immagine in un array di byte

fi = Rjb::import('java.io.File').new(data_dir + "star.png")

file_content = Rjb::import('java.nio.file.Files').readAllBytes(fi.toPath())

forme = diagram.getPages().getPage("Flusso 1").getShapes()

io = 0

 mentre io< shapes.getCount()

    shape = shapes.get(i)

    # Filter shapes by type Foreign

    if shape.getType() == Rjb::import('com.aspose.diagram.TypeValue').FOREIGN

        # replace picture shape

        shape.getForeignData().setValue(file_content)

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "ReplacePictureShape.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Replaced picture shape successfully!"

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Sostituire una forma immagine del Visio Diagram (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/replacepictureshape.rb)
