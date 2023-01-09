---
title: Export Visio Diagram to HTML in Ruby
type: docs
weight: 20
url: /es/java/export-visio-diagram-to-html-in-ruby/
---
## **Aspose.Diagram - Export Visio Diagram to HTML**
To Export Visio Diagram to HTML using **Aspose.Diagram Java para rubí** , simplemente invocar**Exportar a HTML** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as Html

diagram.save(data_dir + "Diagram.html", Rjb::import('com.aspose.diagram.SaveFileFormat').HTML)

puts "Exported visio diagram to HTML."

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Export Visio Diagram to HTML (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttohtml.rb)
