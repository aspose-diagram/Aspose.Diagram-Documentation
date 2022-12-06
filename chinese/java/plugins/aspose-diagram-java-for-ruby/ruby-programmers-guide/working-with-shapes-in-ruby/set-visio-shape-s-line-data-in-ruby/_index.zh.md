---
title: 在 Ruby 中设置 Visio 形状的线数据
type: docs
weight: 140
url: /zh/java/set-visio-shape-s-line-data-in-ruby/
---
## **Aspose.Diagram - 设置 Visio 形状的线数据**
设置 Visio 形状的线数据使用**Aspose.Diagram Java 红宝石** 只需调用**设置形状线数据**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

数据_dir = File.dirname(File.dirname(File.dirname(File.dirname(__文件__)))) + '/数据/'

\# 创建 Diagram 实例

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

形状 = diagram.getPages().getPage(0).getShapes()

我 = 0

当我< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "rectangle" && shape.getID() == 1

        shape.getLine().getLineColor().setValue(diagram.getPages().getPage(0).getShapes().getShape(1).getFill().getFillForegnd().getValue())

        shape.getLine().getLineWeight().setValue(0.07041666666666667)

        shape.getLine().getRounding().setValue(0.1)

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "SetShapeLineData.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set visio shape's line data."

{{< /highlight >}}
## **下载运行代码**
下载**设置 Visio 形状的线数据 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapelinedata.rb)
