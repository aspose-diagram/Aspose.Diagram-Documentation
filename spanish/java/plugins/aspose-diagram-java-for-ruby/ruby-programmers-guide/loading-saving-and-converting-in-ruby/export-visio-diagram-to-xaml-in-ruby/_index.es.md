---
title: Exportar Visio Diagram a XAML en Ruby
type: docs
weight: 60
url: /es/java/export-visio-diagram-to-xaml-in-ruby/
---
## **Aspose.Diagram - Exportar Visio Diagram a XAML**
 Para exportar Visio Diagram a XAML usando**Aspose.Diagram Java para rubí** , simplemente invocar**Exportar a Xaml** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as XAML

diagram.save(data_dir + "Diagram.xaml", Rjb::import('com.aspose.diagram.SaveFileFormat').XAML)

puts "Exported visio diagram to XAML."

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Exportar Visio Diagram a XAML (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoxaml.rb)
