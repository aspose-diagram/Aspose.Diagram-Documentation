﻿---
title: Byt ut en bildform av Visio Diagram i Ruby
type: docs
weight: 60
url: /sv/java/replace-a-picture-shape-of-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Byt ut en bildform på Visio Diagram**
 För att ersätta en bildform på Visio Diagram med**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**ReplacePictureShape** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FIL__)))) + '/data/'

\# Skapa instans av Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# konvertera bilden till byte-array

fi = Rjb::import('java.io.File').new(data_dir + "star.png")

file_content = Rjb::import('java.nio.file.Files').readAllBytes(fi.toPath())

shapes = diagram.getPages().getPage("Flöde 1").getShapes()

i = 0

 medan jag< shapes.getCount()

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
## **Ladda ner Running Code**
 Ladda ner**Byt ut en bildform på Visio Diagram (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/replacepictureshape.rb)
