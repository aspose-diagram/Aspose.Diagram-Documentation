---
title: Exportera Visio Diagram till XML i Ruby
type: docs
weight: 70
url: /sv/java/export-visio-diagram-to-xml-in-ruby/
---
## **Aspose.Diagram - Exporterar VSD till VDX**
För att exportera VSD till VDX med hjälp av**Aspose.Diagram Java för Ruby** , ringa upp**export_to_vdx** metod av**ExportToXml** modul. Här kan du se exempelkod.

**Ruby kod**

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
## **Aspose.Diagram - Exporterar VSD till VSX**
För att exportera VSD till VSX med hjälp av**Aspose.Diagram Java för Ruby** , ringa upp**export_to_vsx** metod av**ExportToXml** modul. Här kan du se exempelkod.

**Ruby kod**

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
## **Aspose.Diagram - Exporterar VSD till VTX**
För att exportera VSD till VTX med hjälp av**Aspose.Diagram Java för Ruby** , ringa upp**export_to_vtx** metod av**ExportToXml** modul. Här kan du se exempelkod.

**Ruby kod**

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
## **Ladda ner Running Code**
 Ladda ner**Exportera Visio Diagram till XML (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoxml.rb)
