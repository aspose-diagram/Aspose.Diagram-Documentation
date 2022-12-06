---
title: Uppdatera Visio Shape Text in Ruby
type: docs
weight: 30
url: /sv/java/update-visio-shape-text-in-ruby/
---
## **Aspose.Diagram - Uppdatering Visio Formtext**
För att uppdatera Visio Forma text med hjälp av**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**UpdateShapeText** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FIL__)))) + '/data/'

\# Skapa instans av Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

shapes = diagram.getPages().getPage(0).getShapes()

i = 0

 medan jag< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process" && shape.getID() == 1

        shape.getText().getValue().clear()

        shape.getText().getValue().add(Rjb::import('com.aspose.diagram.Txt').new("New Text"))

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "UpdateShapeText.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Updated shape text."

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Uppdatera Visio Formtext (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Text/updateshapetext.rb)
