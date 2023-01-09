---
title: Obtener datos de hipervínculo de forma de un dibujo Visio en Ruby
type: docs
weight: 20
url: /es/java/get-shape-hyperlink-data-from-a-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Obtener datos de hipervínculo de forma**
Para obtener datos de hipervínculo de forma usando**Aspose.Diagram Java para rubí** , simplemente invocar**GetShapeHyperlinkData** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 datos_dir = Archivo.dirname(Archivo.dirname(Archivo.dirname(Archivo.dirname(__EXPEDIENTE__)))) + '/datos/'

\# Crear instancia de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Hipervínculos.vdx")

\# Obtener una forma particular

forma = diagram.getPages().getPage("Flujo 1").getShapes().getShape(1)

hipervínculos = forma.getHyperlinks()

yo = 0

 mientras yo< hyperlinks.getCount()

    hyperlink = hyperlinks.get(i)

    puts "Address: " + hyperlink.getAddress().getValue().to_s

    puts "Sub Address: " + hyperlink.getSubAddress().getValue().to_s

    puts "Description: " + hyperlink.getDescription().getValue().to_s

    i +=1

end

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Obtener datos de hipervínculo de forma de un dibujo Visio (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Hyperlinks/getshapehyperlinkdata.rb)
