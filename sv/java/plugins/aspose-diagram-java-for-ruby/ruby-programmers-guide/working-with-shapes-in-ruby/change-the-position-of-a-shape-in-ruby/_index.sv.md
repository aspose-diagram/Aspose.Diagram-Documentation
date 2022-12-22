---
title: Ändra positionen för en form i rubin
type: docs
weight: 10
url: /sv/java/change-the-position-of-a-shape-in-ruby/
---
## **Aspose.Diagram - Ändra positionen för en form**
 För att ändra positionen för en form med hjälp av**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**ChangeShapePosition** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FIL__)))) + '/data/'

\# Skapa instans av Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

shapes = diagram.getPages().getPage(0).getShapes()

i = 0

 medan jag< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process" && shape.getID() == 2

        shape.move(1, 1)

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "ChangeShapePosition.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Changed position of a shape."

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Ändra positionen för en form (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/changeshapeposition.rb)
