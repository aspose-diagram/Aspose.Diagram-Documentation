---
title: 在 Ruby 中将新的空白页插入到 Visio 绘图中
type: docs
weight: 20
url: /zh/java/insert-a-new-blank-page-into-a-visio-drawing-in-ruby/
---
## **Aspose.Diagram - 将新的空白页插入到 Visio 绘图中**
要将新的空白页插入到 Visio 绘图中，请使用**Aspose.Diagram Java 红宝石** 只需调用**添加页面**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

定义初始化（）

数据_dir = File.dirname(File.dirname(File.dirname(File.dirname(__文件__)))) + '/数据/'

 调用 diagram 构造函数从 VSD 文件中加载 diagram

 diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

 # 获取最大页面ID

最大限度_页_编号 = 得到_最大限度_page_id(diagram)

 # 初始化一个新的页面对象

new_page = Rjb::import('com.aspose.diagram.Page').new

 # 设置名称

new_page.setName("新页面")



 # 设置页面ID

新的_page.setID(最大_page_id + 1)

 # 或者尝试页面构造函数

 页面 newPage = new Page(MaxPageId + 1);

 # 添加一个新的空白页

diagram.getPages().add(new_page)

 # 保存 diagram

 diagram.保存（数据_目录+“新页_Output.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

放“添加新页面”。

结尾

定义得到_最大限度_page_id(diagram)

最大值 = diagram.getPages().getPage(0).getID()

我 = 1

当我< diagram.getPages().getCount()

        if max < diagram.getPages().getPage(i).getID()

            max = diagram.getPages().getPage(i).getID()

        end

        i +=1

    end

    return max

end

{{< /highlight >}}
## **下载运行代码**
下载**将新空白页插入 Visio 绘图 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/addpage.rb)
