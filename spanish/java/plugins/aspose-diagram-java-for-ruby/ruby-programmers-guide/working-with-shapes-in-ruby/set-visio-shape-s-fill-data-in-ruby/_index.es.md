---
title: Establezca los datos de relleno de Visio Shape en Ruby
type: docs
weight: 130
url: /es/java/set-visio-shape-s-fill-data-in-ruby/
---
## **Aspose.Diagram - Establecer Visio Datos de relleno de forma**
 Para configurar los datos de relleno de la forma Visio usando**Aspose.Diagram Java para rubí** , simplemente invocar**EstablecerFormaRellenarDatos** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 datos_dir = Archivo.dirname(Archivo.dirname(Archivo.dirname(Archivo.dirname(__EXPEDIENTE__)))) + '/datos/'

\# Crear instancia de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').nuevo(data_dir + "Dibujo.vsd")

formas = diagram.getPages().getPage(0).getShapes()

yo = 0

 mientras yo< shapes.getCount()

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
## **Descargar código de ejecución**
 Descargar**Establecer Visio Datos de relleno de la forma (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapefilldata.rb)
