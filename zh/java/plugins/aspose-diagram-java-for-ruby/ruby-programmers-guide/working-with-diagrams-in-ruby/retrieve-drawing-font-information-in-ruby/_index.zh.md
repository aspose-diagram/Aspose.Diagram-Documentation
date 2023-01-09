---
title: 在 Ruby 中检索绘图字体信息
type: docs
weight: 30
url: /zh/java/retrieve-drawing-font-information-in-ruby/
---
## **Aspose.Diagram - 检索绘图字体信息**
要使用检索绘图字体信息**Aspose.Diagram Java 红宝石** 只需调用**获取图表字体信息**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

数据_dir = File.dirname(File.dirname(File.dirname(File.dirname(__文件__)))) + '/数据/'

\# 创建 Diagram 实例

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

字体 = diagram.getFonts()

我 = 0

当我< fonts.getCount()

    font = fonts.get(i)

    # Display information about the fonts

    puts font.getName()

    i +=1

end

{{< /highlight >}}
## **下载运行代码**
下载**检索绘图字体信息 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/getdiagramfontinfo.rb)
