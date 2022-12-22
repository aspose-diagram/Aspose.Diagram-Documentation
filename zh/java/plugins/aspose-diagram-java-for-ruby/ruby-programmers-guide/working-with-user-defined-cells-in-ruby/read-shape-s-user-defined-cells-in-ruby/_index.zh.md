---
title: 在 Ruby 中读取 Shape 的用户定义单元格
type: docs
weight: 20
url: /zh/java/read-shape-s-user-defined-cells-in-ruby/
---
## **Aspose.Diagram - 读取形状的用户定义单元格**
使用读取形状的用户定义单元格**Aspose.Diagram Java 红宝石** 只需调用**读取用户定义的单元格**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

数据_dir = File.dirname(File.dirname(File.dirname(File.dirname(__文件__)))) + '/数据/'

\# 创建 Diagram 实例

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "UserDefinedCells.vdx")

shapes = diagram.getPages().getPage("Flow 1").getShapes()

我 = 0

当我< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process"

        users = shape.getUsers()

        j = 0

        while j < users.getCount()

            user = users.get(j)

            puts user.getName() + ": " + user.getValue().getVal()

            j +=1

        end

        break

    end

    i +=1

end

{{< /highlight >}}
## **下载运行代码**
下载**读取形状的用户定义单元格 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/readuserdefinedcells.rb)
