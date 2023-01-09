---
title: Hämta Visio Forminformation i Ruby
type: docs
weight: 70
url: /sv/java/retrieve-visio-shape-information-in-ruby/
---
## **Aspose.Diagram - Hämta Visio Forminformation**
 För att hämta Visio Forminformation med hjälp av**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**GetShapeInfo** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FIL__)))) + '/data/'

\# Skapa instans av Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

shapes = diagram.getPages().getPage(0).getShapes()

i = 0

 medan jag< shapes.getCount()

    shape = shapes.get(i)

    # Display information about the shapes

    puts "Shape ID : " + shape.getID().to_s

    puts "Name : " + shape.getName().to_s

    puts "Master Shape : " + shape.getMaster().getName().to_s

    i +=1

end

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Hämta Visio Forminformation (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/getshapeinfo.rb)
