---
title: Crear celda definida por el usuario en ShapeSheet en Ruby
type: docs
weight: 10
url: /es/java/create-user-defined-cell-in-the-shapesheet-in-ruby/
---
## **Aspose.Diagram - Crear celda definida por el usuario en ShapeSheet**
 Para crear una celda definida por el usuario en ShapeSheet usando**Aspose.Diagram Java para rubí** , simplemente invocar**CreateUserDefinedCell** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 datos_dir = Archivo.dirname(Archivo.dirname(Archivo.dirname(Archivo.dirname(__EXPEDIENTE__)))) + '/datos/'

\# Crear instancia de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').nuevo(data_dir + "Dibujo.vsd")

páginas = diagram.getPages()

yo = 0

 mientras yo< pages.getCount()

    page = pages.get(i)

    shapes = page.getShapes()

    j = 0

    while j < shapes.getCount()

        shape = shapes.get(j)

        if shape.getNameU() == "Process"

            # Initialize user object

            user = Rjb::import('com.aspose.diagram.User').new

            user.setName("UserDefineCell")

            user.getValue().setVal("800")

            # Add user-defined cell

            shape.getUsers().add(user)

        end

        j +=1

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "UserDefinedCells.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Created User-defined Cell in the ShapeSheet."

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Crear celda definida por el usuario en ShapeSheet (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/createuserdefinedcell.rb)
