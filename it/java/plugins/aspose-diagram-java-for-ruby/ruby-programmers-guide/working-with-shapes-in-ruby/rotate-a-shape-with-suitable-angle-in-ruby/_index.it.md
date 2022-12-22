---
title: Ruota una forma con un angolo adatto in Ruby
type: docs
weight: 80
url: /it/java/rotate-a-shape-with-suitable-angle-in-ruby/
---
## **Aspose.Diagram - Ruota una forma con un angolo adatto**
 Per ruotare una forma con un angolo adatto usando**Aspose.Diagram Java per Rubino** , semplicemente invocare**Ruota Forma** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

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
## **Scarica il codice in esecuzione**
 Scarica**Ruota una forma con l'angolo adatto (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/rotateshape.rb)
