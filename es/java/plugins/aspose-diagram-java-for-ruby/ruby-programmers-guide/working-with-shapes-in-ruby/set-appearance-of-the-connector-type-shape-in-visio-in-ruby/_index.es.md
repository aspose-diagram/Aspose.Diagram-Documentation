---
title: Establecer la apariencia de la forma del tipo de conector en Visio en Ruby
type: docs
weight: 100
url: /es/java/set-appearance-of-the-connector-type-shape-in-visio-in-ruby/
---
## **Aspose.Diagram - Establecer apariencia de la forma del tipo de conector en Visio**
 Para establecer la apariencia de la forma del tipo de conector en Visio usando**Aspose.Diagram Java para rubí** , simplemente invocar**EstablecerFormaApariencia** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Access a particular page

page = diagram.getPages().getPage("Flow 1")

\# get a particular connector shape

shape = page.getShapes().getShape(1)

\# set dynamic connector appearance

shape.setConnectorsType(Rjb::import('com.aspose.diagram.ConnectorsTypeValue').STRAIGHT_LINES)

\# Save diagram

diagram.save(data_dir + "SetShapeAppearance.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set appearnce of the connector type shape."

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Establecer apariencia de la forma del tipo de conector en Visio (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapeappearance.rb)
