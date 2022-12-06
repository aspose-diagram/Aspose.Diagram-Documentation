---
title: Exportieren Sie Visio Diagram in XML in Ruby
type: docs
weight: 70
url: /de/java/export-visio-diagram-to-xml-in-ruby/
---
## **Aspose.Diagram - Exportieren von VSD bis VDX**
So exportieren Sie VSD bis VDX mit**Aspose.Diagram Java für Rubin** , Anruf**export_to_vdx** Methode von**ExportToXml** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

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
## **Aspose.Diagram - Exportieren von VSD bis VSX**
So exportieren Sie VSD bis VSX mit**Aspose.Diagram Java für Rubin** , Anruf**export_to_vsx** Methode von**ExportToXml** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

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
## **Aspose.Diagram - Exportieren von VSD bis VTX**
So exportieren Sie VSD bis VTX mit**Aspose.Diagram Java für Rubin** , Anruf**export_to_vtx** Methode von**ExportToXml** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

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
## **Laufcode herunterladen**
 Download**Visio Diagram in XML exportieren (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoxml.rb)
