---
title: 从 Ruby 中的 Visio 绘图中获取页面对象
type: docs
weight: 10
url: /zh/java/get-a-page-object-from-visio-drawing-in-ruby/
---
## **Aspose.Diagram - 通过 ID 获取页面对象**
要使用 ID 通过 ID 获取页面对象**Aspose.Diagram Java 红宝石**， 称呼**get_page_object_by_id**的方法**获取页面对象**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

 def get_page_object_by_id() 

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    page_id = 0

    # Get page object by id

    page = diagram.getPages().getPage(page_id)

    puts "Page : " + page.to_string

end

{{< /highlight >}}
## **Aspose.Diagram - 按名称获取页面对象**
要按名称获取页面对象，请使用**Aspose.Diagram Java 红宝石**， 称呼**get_page_object_by_name**的方法**获取页面对象**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

 def get_page_object_by_name() 

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    # Set page name

    page_name = "Flow 1"

    # Get page object by name

    page = diagram.getPages().getPage(page_name)

    puts "Page : " + page.to_string

end

{{< /highlight >}}
## **下载运行代码**
下载**从 Visio 绘图中获取页面对象 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/getpageobject.rb)
