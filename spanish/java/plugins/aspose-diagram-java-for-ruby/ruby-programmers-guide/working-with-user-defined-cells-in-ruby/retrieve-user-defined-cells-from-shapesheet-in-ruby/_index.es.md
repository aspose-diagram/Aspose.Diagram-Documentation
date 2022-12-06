---
title: Recuperar celdas definidas por el usuario de Shapesheet en Ruby
type: docs
weight: 30
url: /es/java/retrieve-user-defined-cells-from-shapesheet-in-ruby/
---
## **Aspose.Diagram - Recuperar celdas definidas por el usuario de Shapesheet**
 Para recuperar celdas definidas por el usuario de Shapesheet usando**Aspose.Diagram Java para rubí** , simplemente invocar**Obtener celdas definidas por el usuario** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 datos_dir = Archivo.dirname(Archivo.dirname(Archivo.dirname(Archivo.dirname(__EXPEDIENTE__)))) + '/datos/'

\# Crear instancia de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "UserDefinedCells.vdx")

páginas = diagram.getPages()

cuenta = 0

 mientras cuenta< pages.getCount()

    page = pages.get(count)

    shapes = page.getShapes()

    i = 0

    while i < shapes.getCount()

        shape = shapes.get(i)

        if shape.getNameU() == "Process"

            users = shape.getUsers()

            j = 0

            while j < users.getCount()

                user = users.get(j)

                            puts "Name: " + user.getNameU() + " Value: " + user.getValue().getVal() + " Prompt: " + user.getPrompt().getValue()

                j +=1

            end

            break

        end

        i +=1

    end

    count +=1

end

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Recuperar celdas definidas por el usuario de Shapesheet (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/getuserdefinedcells.rb)
