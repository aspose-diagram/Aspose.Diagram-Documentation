---
title: 在 Ruby 的 ShapeSheet 中创建用户定义的单元格
type: docs
weight: 10
url: /zh/java/create-user-defined-cell-in-the-shapesheet-in-ruby/
---
## **Aspose.Diagram - 在 ShapeSheet 中创建用户定义的单元格**
在 ShapeSheet 中使用创建用户定义的单元格**Aspose.Diagram Java 红宝石** 只需调用**创建用户定义的单元格**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

数据_dir = File.dirname(File.dirname(File.dirname(File.dirname(__文件__)))) + '/数据/'

\# 创建 Diagram 实例

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

页面 = diagram.getPages()

我 = 0

当我< pages.getCount()

    page = pages.get(i)

    shapes = page.getShapes()

    j = 0

    while j < shapes.getCount()

        shape = shapes.get(j)

        if shape.getNameU() == "Process"

            # Initialize user object

            user = Rjb::import('com.aspose.diagram.User').new

            user.setName("UserDefineCell")

            user.getValue().setVal("800")

            # Add user-defined cell

            shape.getUsers().add(user)

        end

        j +=1

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "UserDefinedCells.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Created User-defined Cell in the ShapeSheet."

{{< /highlight >}}
## **下载运行代码**
下载**在 ShapeSheet 中创建用户定义的单元格 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/createuserdefinedcell.rb)
