---
title: 将 Visio Diagram 导出到 Ruby 中的 XAML
type: docs
weight: 60
url: /zh/java/export-visio-diagram-to-xaml-in-ruby/
---
## **Aspose.Diagram - 将 Visio Diagram 导出到 XAML**
将 Visio Diagram 导出到 XAML 使用**Aspose.Diagram Java 红宝石** 只需调用**导出到 Xaml**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as XAML

diagram.save(data_dir + "Diagram.xaml", Rjb::import('com.aspose.diagram.SaveFileFormat').XAML)

puts "Exported visio diagram to XAML."

{{< /highlight >}}
## **下载运行代码**
下载**将 Visio Diagram 导出到 XAML (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoxaml.rb)
