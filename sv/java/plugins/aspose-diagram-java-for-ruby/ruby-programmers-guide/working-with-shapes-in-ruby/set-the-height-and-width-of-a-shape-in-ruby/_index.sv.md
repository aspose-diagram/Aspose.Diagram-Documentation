---
title: Ställ in höjden och bredden på en form i rubin
type: docs
weight: 120
url: /sv/java/set-the-height-and-width-of-a-shape-in-ruby/
---
## **Aspose.Diagram - Ställ in höjd och bredd på en form**
 För att ställa in höjd och bredd på en form med**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**SetShapeHeightAndWidth** modul. Här kan du se exempelkod.

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

        shape.setWidth(2 * shape.getXForm().getWidth().getValue())

        shape.setHeight(2 * shape.getXForm().getHeight().getValue())

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "SetShapeHeightAndWidth.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set height and width of shape."

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Ställ in höjd och bredd på en form (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapeheightandwidth.rb)
