---
title: Ställ in Visio Shape's Fill-data i Ruby
type: docs
weight: 130
url: /sv/java/set-visio-shape-s-fill-data-in-ruby/
---
## **Aspose.Diagram - Set Visio Shape's Fill data**
 För att ställa in Visio Shape's Fill-data med hjälp av**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**SetShapeFillData** modul. Här kan du se exempelkod.

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

        shape.getFill().getFillBkgnd().setValue(diagram.getPages().getPage(0).getShapes().getShape(0).getFill().getFillBkgnd().getValue())

        shape.getFill().getFillForegnd().setValue("#ebf8df")

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "SetShapeFillData.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set visio shape's fill data."

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Set Visio Shape's Fill data (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapefilldata.rb)
