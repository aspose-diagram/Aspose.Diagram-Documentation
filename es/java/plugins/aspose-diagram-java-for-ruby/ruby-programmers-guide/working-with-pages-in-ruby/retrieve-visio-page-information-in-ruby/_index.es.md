---
title: Recuperar información de la página Visio en Ruby
type: docs
weight: 30
url: /es/java/retrieve-visio-page-information-in-ruby/
---
## **Aspose.Diagram - Recuperar Visio Información de la página**
 Para recuperar la información de la página Visio usando**Aspose.Diagram Java para rubí** , simplemente invocar**ObtenerInfoPágina** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

# page = diagram.getPages().getPage(page_id)

page = diagram.getPages().getPage(0)

puts "Page ID : " + page.getName().to_s

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Recuperar Visio Información de página (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/getpageinfo.rb)
