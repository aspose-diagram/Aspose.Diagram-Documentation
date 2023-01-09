---
title: 在 Ruby 中创建一个空的 Visio Diagram
type: docs
weight: 10
url: /zh/java/create-an-empty-visio-diagram-in-ruby/
---
## **Aspose.Diagram - 创建一个空的 Visio Diagram**
创建一个空的 Visio Diagram 使用**Aspose.Diagram Java 红宝石** 只需调用**创建图表**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new

\# Save as VDX

diagram.save(data_dir + "CreateDiagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Created visio diagram successfully!"

{{< /highlight >}}
## **下载运行代码**
下载**创建一个空的 Visio Diagram (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/creatediagram.rb)
