---
title: 在 Ruby 中更新 Visio 形状文本
type: docs
weight: 30
url: /zh/java/update-visio-shape-text-in-ruby/
---
## **Aspose.Diagram - 更新 Visio 形状文本**
使用更新 Visio 形状文本**Aspose.Diagram Java 红宝石** 只需调用**更新形状文本**模块。在这里您可以看到示例代码。

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

        shape.getText().getValue().clear()

        shape.getText().getValue().add(Rjb::import('com.aspose.diagram.Txt').new("New Text"))

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "UpdateShapeText.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Updated shape text."

{{< /highlight >}}
## **下载运行代码**
下载**更新 Visio 形状文本 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Text/updateshapetext.rb)
