---
title: Export Visio Diagram to XML in Ruby
type: docs
weight: 70
url: /java/export-visio-diagram-to-xml-in-ruby/
---

## **Aspose.Diagram - Exporting VSD to VDX**
To Export VSD to VDX using **Aspose.Diagram Java for Ruby**, call **export_to_vdx** method of **ExportToXml** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

 def export_to_vdx()

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    # Save as VDX

    diagram.save(data_dir + "Diagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

    puts "Exported visio diagram to VDX."

end

{{< /highlight >}}
## **Aspose.Diagram - Exporting VSD to VSX**
To Export VSD to VSX using **Aspose.Diagram Java for Ruby**, call **export_to_vsx** method of **ExportToXml** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

 def export_to_vsx()

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    # Save as VSX

    diagram.save(data_dir + "Diagram.vsx", Rjb::import('com.aspose.diagram.SaveFileFormat').VSX)

    puts "Exported visio diagram to VSX."

end

{{< /highlight >}}
## **Aspose.Diagram - Exporting VSD to VTX**
To Export VSD to VTX using **Aspose.Diagram Java for Ruby**, call **export_to_vtx** method of **ExportToXml** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

 def export_to_vtx()

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    # Save as VTX

    diagram.save(data_dir + "Diagram.vtx", Rjb::import('com.aspose.diagram.SaveFileFormat').VTX)

    puts "Exported visio diagram to VTX."

end

{{< /highlight >}}
## **Download Running Code**
Download **Export Visio Diagram to XML (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoxml.rb)
- [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Export/exporttoxml.rb)
