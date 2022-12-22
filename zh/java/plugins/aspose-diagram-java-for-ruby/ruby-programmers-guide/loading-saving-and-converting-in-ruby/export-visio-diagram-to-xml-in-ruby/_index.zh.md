---
title: 在 Ruby 中将 Visio Diagram 导出到 XML
type: docs
weight: 70
url: /zh/java/export-visio-diagram-to-xml-in-ruby/
---
## **Aspose.Diagram - 出口 VSD 到 VDX**
将 VSD 导出到 VDX 使用**Aspose.Diagram Java 红宝石**， 称呼**export_to_vdx**的方法**导出到Xml**模块。在这里您可以看到示例代码。

**红宝石代码**

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
## **Aspose.Diagram - 出口 VSD 到 VSX**
将 VSD 导出到 VSX 使用**Aspose.Diagram Java 红宝石**， 称呼**export_to_vsx**的方法**导出到Xml**模块。在这里您可以看到示例代码。

**红宝石代码**

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
## **Aspose.Diagram - 出口 VSD 到 VTX**
将 VSD 导出到 VTX 使用**Aspose.Diagram Java 红宝石**， 称呼**export_to_vtx**的方法**导出到Xml**模块。在这里您可以看到示例代码。

**红宝石代码**

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
## **下载运行代码**
下载**将 Visio Diagram 导出到 XML (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoxml.rb)
