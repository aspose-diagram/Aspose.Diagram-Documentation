---
title: Agregue una nueva capa en el Visio Diagram en Ruby
type: docs
weight: 10
url: /es/java/add-a-new-layer-in-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Agregar una nueva capa**
 Para agregar una nueva capa usando**Aspose.Diagram Java para rubí** , simplemente invocar**AñadirNuevaCapa** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Basic_Shapes.vsd")

\# get Visio page

page = diagram.getPages().getPage(0)

\# initialize a new Layer class object

layer = Rjb::import('com.aspose.diagram.Layer').new

\# set Layer name

layer.getName().setValue("Layer2")

\# set Layer Visibility

layer.getVisible().setValue(2)

\# add Layer to the particular page sheet

page.getPageSheet().getLayers().add(layer)

\# add a new shape

shape_id = page.addShape(3.0, 3.0, 0.36, 0.36, "Circle")

\# get the Shape object

shape = page.getShapes().getShape(shape_id)

\# assign this new Layer

shape.getLayerMem().getLayerMember().setValue(layer.getIX().to_s)

\# Save diagram

diagram.save(data_dir + "AddNewLayer.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Added a new Layer in the Visio Diagram."

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Agregue una nueva capa en el Visio Diagram (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Layers/addnewlayer.rb)
