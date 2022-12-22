---
title: Exportar Visio Diagram a XML en Ruby
type: docs
weight: 70
url: /es/java/export-visio-diagram-to-xml-in-ruby/
---
## **Aspose.Diagram - Exportando VSD a VDX**
Para exportar VSD a VDX usando**Aspose.Diagram Java para rubí** , llamar**exportar_a_vdx** método de**Exportar a Xml** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 def export_to_vdx()

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    # Save as VDX

    diagram.save(data_dir + "Diagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

    puts "Exported visio diagram to VDX."

end

{{< /highlight >}}
## **Aspose.Diagram - Exportando VSD a VSX**
Para exportar VSD a VSX usando**Aspose.Diagram Java para rubí** , llamar**exportar_a_vsx** método de**Exportar a Xml** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 def export_to_vsx()

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    # Save as VSX

    diagram.save(data_dir + "Diagram.vsx", Rjb::import('com.aspose.diagram.SaveFileFormat').VSX)

    puts "Exported visio diagram to VSX."

end

{{< /highlight >}}
## **Aspose.Diagram - Exportando VSD a VTX**
Para exportar VSD a VTX usando**Aspose.Diagram Java para rubí** , llamar**exportar_a_vtx** método de**Exportar a Xml** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 def export_to_vtx()

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    # Save as VTX

    diagram.save(data_dir + "Diagram.vtx", Rjb::import('com.aspose.diagram.SaveFileFormat').VTX)

    puts "Exported visio diagram to VTX."

end

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Exportar Visio Diagram a XML (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoxml.rb)
