---
title: 从 Ruby 中的 Visio 绘图中获取形状超链接数据
type: docs
weight: 20
url: /zh/java/get-shape-hyperlink-data-from-a-visio-drawing-in-ruby/
---
## **Aspose.Diagram - 获取形状超链接数据**
获取形状超链接数据使用**Aspose.Diagram Java 红宝石** 只需调用**获取形状超链接数据**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

数据_dir = File.dirname(File.dirname(File.dirname(File.dirname(__文件__)))) + '/数据/'

\# 创建 Diagram 实例

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Hyperlinks.vdx")

\# 得到一个特定的形状

shape = diagram.getPages().getPage("Flow 1").getShapes().getShape(1)

超链接 = shape.getHyperlinks()

我 = 0

当我< hyperlinks.getCount()

    hyperlink = hyperlinks.get(i)

    puts "Address: " + hyperlink.getAddress().getValue().to_s

    puts "Sub Address: " + hyperlink.getSubAddress().getValue().to_s

    puts "Description: " + hyperlink.getDescription().getValue().to_s

    i +=1

end

{{< /highlight >}}
## **下载运行代码**
下载**从 Visio 绘图中获取形状超链接数据 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Hyperlinks/getshapehyperlinkdata.rb)
