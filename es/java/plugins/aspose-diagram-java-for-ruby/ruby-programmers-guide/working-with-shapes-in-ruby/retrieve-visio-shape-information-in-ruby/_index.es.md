---
title: Recuperar información de forma Visio en Ruby
type: docs
weight: 70
url: /es/java/retrieve-visio-shape-information-in-ruby/
---
## **Aspose.Diagram - Recuperar Visio Información de forma**
 Para recuperar información de la forma Visio usando**Aspose.Diagram Java para rubí** , simplemente invocar**ObtenerInfoForma** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 datos_dir = Archivo.dirname(Archivo.dirname(Archivo.dirname(Archivo.dirname(__EXPEDIENTE__)))) + '/datos/'

\# Crear instancia de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').nuevo(data_dir + "Dibujo.vsd")

formas = diagram.getPages().getPage(0).getShapes()

yo = 0

 mientras yo< shapes.getCount()

    shape = shapes.get(i)

    # Display information about the shapes

    puts "Shape ID : " + shape.getID().to_s

    puts "Name : " + shape.getName().to_s

    puts "Master Shape : " + shape.getMaster().getName().to_s

    i +=1

end

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Recuperar Visio Información de forma (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/getshapeinfo.rb)
