---
title: Exportar Visio Diagram a Imagen en Ruby
type: docs
weight: 30
url: /es/java/export-visio-diagram-to-image-in-ruby/
---
## **Aspose.Diagram - Exportar Visio Diagram a imagen**
 Para exportar Visio Diagram a imagen usando**Aspose.Diagram Java para rubí** , simplemente invocar**Exportar a imagen** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as PNG

diagram.save(data_dir + "Diagram.png", Rjb::import('com.aspose.diagram.SaveFileFormat').PNG)

puts "Exported visio diagram to PNG."

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Exportar Visio Diagram a Imagen (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoimage.rb)
