---
title: Lea las celdas definidas por el usuario de Shape en Ruby
type: docs
weight: 20
url: /es/java/read-shape-s-user-defined-cells-in-ruby/
---
## **Aspose.Diagram - Leer celdas definidas por el usuario de Shape**
 Para leer las celdas definidas por el usuario de Shape usando**Aspose.Diagram Java para rubí** , simplemente invocar**Leer celdas definidas por el usuario** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 datos_dir = Archivo.dirname(Archivo.dirname(Archivo.dirname(Archivo.dirname(__EXPEDIENTE__)))) + '/datos/'

\# Crear instancia de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "UserDefinedCells.vdx")

formas = diagram.getPages().getPage("Flow 1").getShapes()

yo = 0

 mientras yo< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process"

        users = shape.getUsers()

        j = 0

        while j < users.getCount()

            user = users.get(j)

            puts user.getName() + ": " + user.getValue().getVal()

            j +=1

        end

        break

    end

    i +=1

end

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Leer las celdas definidas por el usuario de Shape (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/readuserdefinedcells.rb)
