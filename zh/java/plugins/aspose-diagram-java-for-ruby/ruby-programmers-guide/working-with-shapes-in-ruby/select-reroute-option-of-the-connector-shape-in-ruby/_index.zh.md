---
title: 在 Ruby 中选择连接器形状的重新布线选项
type: docs
weight: 90
url: /zh/java/select-reroute-option-of-the-connector-shape-in-ruby/
---
## **Aspose.Diagram - 选择连接器形状的重新布线选项**
要选择连接器形状的重新布线选项，请使用**Aspose.Diagram Java 红宝石** 只需调用**选择重新路由选项**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Access a particular page

page = diagram.getPages().getPage("Flow 1")

\# get a particular connector shape

shape = page.getShapes().getShape(1)

\# set reroute option

shape.getLayout().getConFixedCode().setValue(Rjb::import('com.aspose.diagram.ConFixedCodeValue').NEVER_REROUTE)

\# Save diagram

diagram.save(data_dir + "SelectRerouteOption.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Seleted reroute option of the connector shape."

{{< /highlight >}}
## **下载运行代码**
下载**选择连接器形状的重新布线选项 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/selectrerouteoption.rb)
