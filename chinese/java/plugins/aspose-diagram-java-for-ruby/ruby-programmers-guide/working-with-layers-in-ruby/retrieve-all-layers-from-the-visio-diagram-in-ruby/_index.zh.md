---
title: 从 Ruby 中的 Visio Diagram 中检索所有图层
type: docs
weight: 30
url: /zh/java/retrieve-all-layers-from-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - 检索所有图层**
检索所有图层使用**Aspose.Diagram Java 红宝石** 只需调用**获取所有图层**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

数据_dir = File.dirname(File.dirname(File.dirname(File.dirname(__文件__)))) + '/数据/'

\# 创建 Diagram 实例

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# 得到 Visio 页

页 = diagram.getPages().getPage(0)

图层 = page.getPageSheet().getLayers()

我 = 0

当我< layers.getCount()

    layer = layers.get(i)

    puts "Name: " + layer.getName().getValue().to_s

    puts "Visibility: " + layer.getVisible().getValue().to_s

    puts "Status: " + layer.getStatus().getValue().to_s



    i +=1

end

{{< /highlight >}}
## **下载运行代码**
下载**从 Visio Diagram (Aspose.Diagram) 中检索所有图层**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Layers/getalllayers.rb)
