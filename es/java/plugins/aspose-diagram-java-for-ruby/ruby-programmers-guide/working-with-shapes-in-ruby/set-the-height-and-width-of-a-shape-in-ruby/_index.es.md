---
title: Establecer la altura y el ancho de una forma en Ruby
type: docs
weight: 120
url: /es/java/set-the-height-and-width-of-a-shape-in-ruby/
---
## **Aspose.Diagram - Establecer la altura y el ancho de una forma**
 Para establecer la altura y el ancho de una forma usando**Aspose.Diagram Java para rubí** , simplemente invocar**EstablecerFormaAlturaYAncho** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 datos_dir = Archivo.dirname(Archivo.dirname(Archivo.dirname(Archivo.dirname(__EXPEDIENTE__)))) + '/datos/'

\# Crear instancia de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').nuevo(data_dir + "Dibujo.vsd")

formas = diagram.getPages().getPage(0).getShapes()

yo = 0

 mientras yo< shapes.getCount()

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
## **Descargar código de ejecución**
 Descargar**Establecer la altura y el ancho de una forma (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapeheightandwidth.rb)
