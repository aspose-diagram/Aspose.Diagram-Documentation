---
title: 在 Visio 中用 Ruby 中的图层配置形状对象
type: docs
weight: 20
url: /zh/java/configure-shape-objects-with-layers-in-visio-in-ruby/
---
## **Aspose.Diagram - 使用图层配置形状对象**
使用层配置形状对象**Aspose.Diagram Java 红宝石** 只需调用**ConfigureShapeWithLayers**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

数据_dir = File.dirname(File.dirname(File.dirname(File.dirname(__文件__)))) + '/数据/'

\# 创建 Diagram 实例

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

shapes = diagram.getPages().getPage("Flow 1").getShapes()

我 = 0

当我< shapes.getCount()

    shape = shapes.get(i)

    #puts shape.getName().to_s

    if shape.getName() == "Process"

        # Add shape1 in first two layers. Here "0;1" are indexes of the layers

        layer = shape.getLayerMem()

        layer.getLayerMember().setValue("0;1")

    elsif shape.getName() == "Preparation"

        # Remove shape2 from all the layers

        layer = shape.getLayerMem()

        layer.getLayerMember().setValue("")

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "Layers.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Configured Shape Objects with Layers in Visio."

{{< /highlight >}}
## **下载运行代码**
下载**在 Visio (Aspose.Diagram) 中使用层配置形状对象**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Layers/configureshapewithlayers.rb)
