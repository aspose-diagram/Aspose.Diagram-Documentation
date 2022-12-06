---
title: Leer Visio datos de formas en Ruby
type: docs
weight: 50
url: /es/java/read-visio-shape-data-in-ruby/
---
## **Aspose.Diagram - Leer todas las propiedades de forma**
 Para leer todas las propiedades de forma usando**Aspose.Diagram Java para rubí** , llamar**read_all_shape_properties** método de**LeerFormaDatos** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 definitivamente leer_todos_propiedades_de_forma()

 datos_dir = Archivo.dirname(Archivo.dirname(Archivo.dirname(Archivo.dirname(__EXPEDIENTE__)))) + '/datos/'

 # Crear instancia de Diagram

 diagram = Rjb::import('com.aspose.diagram.Diagram').nuevo(data_dir + "Dibujo.vsd")

 formas = diagram.getPages().getPage(0).getShapes()



 yo = 0

 mientras yo< shapes.getCount()

        shape = shapes.get(i)

        if shape.getName() == "Process"

            j = 0

            while j < shape.getProps().getCount()

                property = shape.getProps().get(j)

                puts property.getLabel().getValue() + ": " + property.getValue().getVal()

                j +=1

            end

            break

        end

        i +=1

    end

end

{{< /highlight >}}
## **Aspose.Diagram - Leer una propiedad de forma por nombre**
 Para leer una propiedad de forma por nombre usando**Aspose.Diagram Java para rubí** , llamar**leer_forma_propiedad_por_nombre** método de**LeerFormaDatos** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 definitivamente leer_forma_propiedad_por_nombre()

 datos_dir = Archivo.dirname(Archivo.dirname(Archivo.dirname(Archivo.dirname(__EXPEDIENTE__)))) + '/datos/'

 # Crear instancia de Diagram

 diagram = Rjb::import('com.aspose.diagram.Diagram').nuevo(data_dir + "Dibujo.vsd")

 formas = diagram.getPages().getPage(0).getShapes()



 yo = 0

 mientras yo< shapes.getCount()

        shape = shapes.get(i)

        if shape.getName() == "Process"

            property = shape.getProps().getProp("Cost")

            puts property.getLabel().getValue() + ": " + property.getValue().getVal()

        end

        i +=1

    end

end

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Leer Visio Datos de forma (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/readshapedata.rb)
