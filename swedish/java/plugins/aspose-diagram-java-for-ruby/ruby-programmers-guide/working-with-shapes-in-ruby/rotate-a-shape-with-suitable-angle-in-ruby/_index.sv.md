---
title: Rotera en form med lämplig vinkel i rubin
type: docs
weight: 80
url: /sv/java/rotate-a-shape-with-suitable-angle-in-ruby/
---
## **Aspose.Diagram - Rotera en form med lämplig vinkel**
 Att rotera en form med lämplig vinkel med hjälp av**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**Rotera form** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Add a shape and set the angle

diagram.getPages().getPage(0).getShapes().getShape(1).setAngle(190)

\# Save diagram

diagram.save(data_dir + "RotateShape.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Rotated shape."

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Rotera en form med lämplig vinkel (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/rotateshape.rb)
