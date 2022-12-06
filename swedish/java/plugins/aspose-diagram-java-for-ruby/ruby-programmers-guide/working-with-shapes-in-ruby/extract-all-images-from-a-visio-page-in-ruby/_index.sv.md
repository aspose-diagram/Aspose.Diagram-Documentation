---
title: Extrahera alla bilder från en Visio-sida i Ruby
type: docs
weight: 30
url: /sv/java/extract-all-images-from-a-visio-page-in-ruby/
---
## **Aspose.Diagram - Extrahera alla bilder från en Visio sida**
 Att extrahera alla bilder från en Visio sida med hjälp av**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**Extrahera bilder** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FIL__)))) + '/data/'

\# Skapa instans av Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

shapes = diagram.getPages().getPage("Flöde 1").getShapes()

i = 0

 medan jag< shapes.getCount()

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
## **Ladda ner Running Code**
 Ladda ner**Extrahera alla bilder från en Visio sida (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/extractimages.rb)
