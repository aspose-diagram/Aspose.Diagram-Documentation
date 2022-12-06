---
title: Exportar Visio Diagram a SVG en Ruby
type: docs
weight: 50
url: /es/java/export-visio-diagram-to-svg-in-ruby/
---
## **Aspose.Diagram - Exportar Visio Diagram a SVG**
 Para exportar Visio Diagram a SVG usando**Aspose.Diagram Java para rubí** , simplemente invocar**Exportar a SVG** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as SVG

diagram.save(data_dir + "Diagram.svg", Rjb::import('com.aspose.diagram.SaveFileFormat').SVG)

puts "Exported visio diagram to SVG."

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Exportar Visio Diagram a SVG (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttosvg.rb)
