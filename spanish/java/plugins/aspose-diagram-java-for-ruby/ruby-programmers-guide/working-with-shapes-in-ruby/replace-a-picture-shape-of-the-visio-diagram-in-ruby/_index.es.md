---
title: Reemplace una forma de imagen de Visio Diagram en Ruby
type: docs
weight: 60
url: /es/java/replace-a-picture-shape-of-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Reemplace una forma de imagen de Visio Diagram**
 Para reemplazar una forma de imagen de Visio Diagram usando**Aspose.Diagram Java para rubí** , simplemente invocar**ReemplazarImagenForma** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 datos_dir = Archivo.dirname(Archivo.dirname(Archivo.dirname(Archivo.dirname(__EXPEDIENTE__)))) + '/datos/'

\# Crear instancia de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').nuevo(data_dir + "Dibujo.vsd")

\# convertir la imagen en una matriz de bytes

fi = Rjb::import('java.io.File').new(data_dir + "star.png")

contenido_archivo = Rjb::import('java.nio.file.Files').readAllBytes(fi.toPath())

formas = diagram.getPages().getPage("Flow 1").getShapes()

yo = 0

 mientras yo< shapes.getCount()

    shape = shapes.get(i)

    # Filter shapes by type Foreign

    if shape.getType() == Rjb::import('com.aspose.diagram.TypeValue').FOREIGN

        # replace picture shape

        shape.getForeignData().setValue(file_content)

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "ReplacePictureShape.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Replaced picture shape successfully!"

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Reemplace una forma de imagen del Visio Diagram (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/replacepictureshape.rb)
