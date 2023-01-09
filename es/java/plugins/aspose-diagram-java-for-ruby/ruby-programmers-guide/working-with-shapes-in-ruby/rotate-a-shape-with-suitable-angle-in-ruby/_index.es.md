---
title: Girar una forma con ángulo adecuado en Ruby
type: docs
weight: 80
url: /es/java/rotate-a-shape-with-suitable-angle-in-ruby/
---
## **Aspose.Diagram - Girar una forma con el ángulo adecuado**
 Para rotar una forma con un ángulo adecuado usando**Aspose.Diagram Java para rubí** , simplemente invocar**RotarForma** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

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
## **Descargar código de ejecución**
 Descargar**Girar una forma con ángulo adecuado (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/rotateshape.rb)
