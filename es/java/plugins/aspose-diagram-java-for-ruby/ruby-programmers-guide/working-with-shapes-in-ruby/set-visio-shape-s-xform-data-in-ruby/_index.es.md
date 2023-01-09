---
title: Establezca los datos XForm de Visio Shape en Ruby
type: docs
weight: 150
url: /es/java/set-visio-shape-s-xform-data-in-ruby/
---
## **Aspose.Diagram - Establecer Visio Datos XForm de Shape**
 Para configurar los datos XForm de Visio Shape usando**Aspose.Diagram Java para rubí** , simplemente invocar**EstablecerFormaXFormarDatos** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 datos_dir = Archivo.dirname(Archivo.dirname(Archivo.dirname(Archivo.dirname(__EXPEDIENTE__)))) + '/datos/'

\# Crear instancia de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').nuevo(data_dir + "Dibujo.vsd")

formas = diagram.getPages().getPage(0).getShapes()

yo = 0

 mientras yo< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "process" && shape.getID() == 1

        shape.getXForm().getPinX().setValue(5)

        shape.getXForm().getPinY().setValue(5)

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "SetShapeXFormData.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set visio shape's XForm data."

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Establecer Visio Datos XForm de Shape (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapexformdata.rb)
