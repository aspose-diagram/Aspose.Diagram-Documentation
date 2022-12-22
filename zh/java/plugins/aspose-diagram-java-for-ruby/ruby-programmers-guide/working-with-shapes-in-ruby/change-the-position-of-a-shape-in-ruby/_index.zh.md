---
title: 在 Ruby 中更改形状的位置
type: docs
weight: 10
url: /zh/java/change-the-position-of-a-shape-in-ruby/
---
## **Aspose.Diagram - 更改形状的位置**
要使用更改形状的位置**Aspose.Diagram Java 红宝石** 只需调用**改变形状位置**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

数据_dir = File.dirname(File.dirname(File.dirname(File.dirname(__文件__)))) + '/数据/'

\# 创建 Diagram 实例

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

形状 = diagram.getPages().getPage(0).getShapes()

我 = 0

当我< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process" && shape.getID() == 2

        shape.move(1, 1)

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "ChangeShapePosition.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Changed position of a shape."

{{< /highlight >}}
## **下载运行代码**
下载**更改形状的位置 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/changeshapeposition.rb)
