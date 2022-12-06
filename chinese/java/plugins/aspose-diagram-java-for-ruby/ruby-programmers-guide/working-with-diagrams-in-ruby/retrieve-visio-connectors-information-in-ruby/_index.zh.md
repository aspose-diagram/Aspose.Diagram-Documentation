---
title: 在 Ruby 中检索 Visio 连接器信息
type: docs
weight: 20
url: /zh/java/retrieve-visio-connectors-information-in-ruby/
---
## **Aspose.Diagram - 检索 Visio 连接器信息**
检索 Visio 连接器信息使用**Aspose.Diagram Java 红宝石** 只需调用**获取连接器信息**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

数据_dir = File.dirname(File.dirname(File.dirname(File.dirname(__文件__)))) + '/数据/'

\# 创建 Diagram 实例

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

连接器 = diagram.getPages().getPage(0).getConnects()

我 = 0

当我< connectors.getCount()

    connector = connectors.get(i)

    # Display information about the Connectors

    puts "From Shape ID : " + connector.getFromSheet().to_s

    puts "To Shape ID : " + connector.getToSheet().to_s

    i +=1

end

{{< /highlight >}}
## **下载运行代码**
下载**检索 Visio 连接器信息 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/getconnectorsinfo.rb)

