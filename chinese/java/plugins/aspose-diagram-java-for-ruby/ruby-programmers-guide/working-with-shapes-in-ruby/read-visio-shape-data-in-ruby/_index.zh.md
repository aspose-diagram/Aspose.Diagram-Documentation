---
title: 在 Ruby 中读取 Visio 形状数据
type: docs
weight: 50
url: /zh/java/read-visio-shape-data-in-ruby/
---
## **Aspose.Diagram - 读取所有形状属性**
使用读取所有形状属性**Aspose.Diagram Java 红宝石**， 称呼**读取所有形状属性**的方法**读取形状数据**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

定义读取_全部_形状属性（）

数据_dir = File.dirname(File.dirname(File.dirname(File.dirname(__文件__)))) + '/数据/'

 # 创建 Diagram 实例

 diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

形状 = diagram.getPages().getPage(0).getShapes()



我 = 0

当我< shapes.getCount()

        shape = shapes.get(i)

        if shape.getName() == "Process"

            j = 0

            while j < shape.getProps().getCount()

                property = shape.getProps().get(j)

                puts property.getLabel().getValue() + ": " + property.getValue().getVal()

                j +=1

            end

            break

        end

        i +=1

    end

end

{{< /highlight >}}
## **Aspose.Diagram - 按名称读取形状属性**
要按名称读取形状属性，请使用**Aspose.Diagram Java 红宝石**， 称呼**按名称读取形状属性**的方法**读取形状数据**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

定义读取_形状_财产_经过_姓名（）

数据_dir = File.dirname(File.dirname(File.dirname(File.dirname(__文件__)))) + '/数据/'

 # 创建 Diagram 实例

 diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

形状 = diagram.getPages().getPage(0).getShapes()



我 = 0

当我< shapes.getCount()

        shape = shapes.get(i)

        if shape.getName() == "Process"

            property = shape.getProps().getProp("Cost")

            puts property.getLabel().getValue() + ": " + property.getValue().getVal()

        end

        i +=1

    end

end

{{< /highlight >}}
## **下载运行代码**
下载**读取 Visio 形状数据 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/readshapedata.rb)
