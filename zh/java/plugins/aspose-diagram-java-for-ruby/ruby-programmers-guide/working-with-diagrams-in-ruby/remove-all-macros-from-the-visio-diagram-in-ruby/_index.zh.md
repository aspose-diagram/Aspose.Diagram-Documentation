---
title: 从 Ruby 中的 Visio Diagram 中删除所有宏
type: docs
weight: 50
url: /zh/java/remove-all-macros-from-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - 从 Visio Diagram 中删除所有宏**
要使用 Visio Diagram 删除所有宏**Aspose.Diagram Java 红宝石** 只需调用**从图表中移除所有宏**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# remove all macros

diagram.setVbProjectData(nil)

\# Save as VDX

diagram.save(data_dir + "RemoveAllMacros.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Removed all macros from diagram successfully!"

{{< /highlight >}}
## **下载运行代码**
下载**从 Visio Diagram (Aspose.Diagram) 中删除所有宏**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/removeallmacrosfromdiagram.rb)
