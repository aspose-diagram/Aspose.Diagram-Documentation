---
title: Export Visio Diagram to HTML in Ruby
type: docs
weight: 20
url: /zh/java/export-visio-diagram-to-html-in-ruby/
---
## **Aspose.Diagram - Export Visio Diagram to HTML**
To Export Visio Diagram to HTML using **Aspose.Diagram Java 红宝石** 只需调用**导出到 HTML**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as Html

diagram.save(data_dir + "Diagram.html", Rjb::import('com.aspose.diagram.SaveFileFormat').HTML)

puts "Exported visio diagram to HTML."

{{< /highlight >}}
## **下载运行代码**
下载**Export Visio Diagram to HTML (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttohtml.rb)
