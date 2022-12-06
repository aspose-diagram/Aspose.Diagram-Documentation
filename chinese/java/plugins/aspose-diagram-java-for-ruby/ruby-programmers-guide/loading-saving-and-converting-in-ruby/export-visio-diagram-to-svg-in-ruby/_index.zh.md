---
title: Export Visio Diagram to SVG in Ruby
type: docs
weight: 50
url: /zh/java/export-visio-diagram-to-svg-in-ruby/
---
## **Aspose.Diagram - Export Visio Diagram to SVG**
To Export Visio Diagram to SVG using **Aspose.Diagram Java 红宝石** 只需调用**导出到 Svg**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as SVG

diagram.save(data_dir + "Diagram.svg", Rjb::import('com.aspose.diagram.SaveFileFormat').SVG)

puts "Exported visio diagram to SVG."

{{< /highlight >}}
## **下载运行代码**
下载**Export Visio Diagram to SVG (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttosvg.rb)
