---
title: 在 Ruby 中检索 Visio 页面信息
type: docs
weight: 30
url: /zh/java/retrieve-visio-page-information-in-ruby/
---
## **Aspose.Diagram - 检索 Visio 页面信息**
检索 Visio 页面信息使用**Aspose.Diagram Java 红宝石** 只需调用**获取页面信息**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

# page = diagram.getPages().getPage(page_id)

page = diagram.getPages().getPage(0)

puts "Page ID : " + page.getName().to_s

{{< /highlight >}}
## **下载运行代码**
下载**检索 Visio 页面信息 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/getpageinfo.rb)
