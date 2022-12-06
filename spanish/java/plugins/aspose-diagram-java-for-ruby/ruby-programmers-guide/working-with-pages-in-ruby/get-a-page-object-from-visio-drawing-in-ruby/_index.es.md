---
title: Obtenga un objeto de página de Visio Dibujo en Ruby
type: docs
weight: 10
url: /es/java/get-a-page-object-from-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Obtener un objeto de página por ID**
 Para obtener un objeto de página por ID usando**Aspose.Diagram Java para rubí** , llamar**get_page_object_by_id** método de**ObtenerObjetoPágina** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 def get_page_object_by_id() 

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    page_id = 0

    # Get page object by id

    page = diagram.getPages().getPage(page_id)

    puts "Page : " + page.to_string

end

{{< /highlight >}}
## **Aspose.Diagram - Obtener un objeto de página por nombre**
 Para obtener un objeto de página por nombre usando**Aspose.Diagram Java para rubí** , llamar**get_page_object_by_name** método de**ObtenerObjetoPágina** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 def get_page_object_by_name() 

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    # Set page name

    page_name = "Flow 1"

    # Get page object by name

    page = diagram.getPages().getPage(page_name)

    puts "Page : " + page.to_string

end

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Obtenga un objeto de página del dibujo Visio (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/getpageobject.rb)
