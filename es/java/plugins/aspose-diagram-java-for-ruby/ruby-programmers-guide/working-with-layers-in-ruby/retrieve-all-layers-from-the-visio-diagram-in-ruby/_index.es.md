---
title: Recuperar todas las capas del Visio Diagram en Ruby
type: docs
weight: 30
url: /es/java/retrieve-all-layers-from-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Recuperar todas las capas**
 Para recuperar todas las capas usando**Aspose.Diagram Java para rubí** , simplemente invocar**ObtenerTodasLasCapas** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 datos_dir = Archivo.dirname(Archivo.dirname(Archivo.dirname(Archivo.dirname(__EXPEDIENTE__)))) + '/datos/'

\# Crear instancia de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').nuevo(data_dir + "Dibujo.vsd")

\# obtener Visio página

página = diagram.getPages().getPage(0)

capas = página.getPageSheet().getLayers()

yo = 0

 mientras yo< layers.getCount()

    layer = layers.get(i)

    puts "Name: " + layer.getName().getValue().to_s

    puts "Visibility: " + layer.getVisible().getValue().to_s

    puts "Status: " + layer.getStatus().getValue().to_s



    i +=1

end

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Recuperar todas las capas del Visio Diagram (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Layers/getalllayers.rb)
