---
title: Ställ in Visio Shape's Line Data i Ruby
type: docs
weight: 140
url: /sv/java/set-visio-shape-s-line-data-in-ruby/
---
## **Aspose.Diagram - Ställ in Visio Shape's Line Data**
 För att ställa in Visio Shapes linjedata med hjälp av**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**SetShapeLineData** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FIL__)))) + '/data/'

\# Skapa instans av Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

shapes = diagram.getPages().getPage(0).getShapes()

i = 0

 medan jag< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "rectangle" && shape.getID() == 1

        shape.getLine().getLineColor().setValue(diagram.getPages().getPage(0).getShapes().getShape(1).getFill().getFillForegnd().getValue())

        shape.getLine().getLineWeight().setValue(0.07041666666666667)

        shape.getLine().getRounding().setValue(0.1)

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "SetShapeLineData.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set visio shape's line data."

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Ställ in Visio Shape's Line Data (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapelinedata.rb)
