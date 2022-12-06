---
title: Export Visio Diagram to XPS in Ruby
type: docs
weight: 80
url: /es/java/export-visio-diagram-to-xps-in-ruby/
---
## **Aspose.Diagram - Export Visio Diagram to XPS**
To Export Visio Diagram to XPS using **Aspose.Diagram Java para rubí** , simplemente invocar**Exportar aXps** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as XPS

diagram.save(data_dir + "Diagram.xps", Rjb::import('com.aspose.diagram.SaveFileFormat').XPS)

puts "Exported visio diagram to XPS."

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Export Visio Diagram to XPS (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoxps.rb)
