---
title: 在 Ruby 中设置形状的高度和宽度
type: docs
weight: 120
url: /zh/java/set-the-height-and-width-of-a-shape-in-ruby/
---
## **Aspose.Diagram - 设置形状的高度和宽度**
设置形状的高度和宽度使用**Aspose.Diagram Java 红宝石** 只需调用**设置形状高度和宽度**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

数据_dir = File.dirname(File.dirname(File.dirname(File.dirname(__文件__)))) + '/数据/'

\# 创建 Diagram 实例

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

形状 = diagram.getPages().getPage(0).getShapes()

我 = 0

当我< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process" && shape.getID() == 1

        shape.setWidth(2 * shape.getXForm().getWidth().getValue())

        shape.setHeight(2 * shape.getXForm().getHeight().getValue())

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "SetShapeHeightAndWidth.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set height and width of shape."

{{< /highlight >}}
## **下载运行代码**
下载**设置形状的高度和宽度 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapeheightandwidth.rb)
