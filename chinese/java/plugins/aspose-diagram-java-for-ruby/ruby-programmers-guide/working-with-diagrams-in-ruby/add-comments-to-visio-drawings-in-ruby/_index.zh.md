---
title: 在 Ruby 中为 Visio 绘图添加评论
type: docs
weight: 40
url: /zh/java/add-comments-to-visio-drawings-in-ruby/
---
## **Aspose.Diagram - 为 Visio 图纸添加注释**
使用以下方法向 Visio 工程图添加注释**Aspose.Diagram Java 红宝石** 只需调用**添加注释到图表**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Add comment

diagram.getPages().getPage(0).addComment(7.205905511811023, 3.880708661417323, "test@")

\# Save as VDX

diagram.save(data_dir + "AddComment.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Added comment successfully!"

{{< /highlight >}}
## **下载运行代码**
下载**添加评论到 Visio 图纸 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/addcommenttodiagram.rb)
