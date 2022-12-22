---
title: 在Ruby中替换Visio Diagram的图片形状
type: docs
weight: 60
url: /zh/java/replace-a-picture-shape-of-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - 替换 Visio 的图片形状 Diagram**
要使用 Visio Diagram 替换图片形状**Aspose.Diagram Java 红宝石** 只需调用**替换图片形状**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

数据_dir = File.dirname(File.dirname(File.dirname(File.dirname(__文件__)))) + '/数据/'

\# 创建 Diagram 实例

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# 将图像转换为字节数组

fi = Rjb::import('java.io.File').new(data_dir + "star.png")

file_content = Rjb::import('java.nio.file.Files').readAllBytes(fi.toPath())

shapes = diagram.getPages().getPage("Flow 1").getShapes()

我 = 0

当我< shapes.getCount()

    shape = shapes.get(i)

    # Filter shapes by type Foreign

    if shape.getType() == Rjb::import('com.aspose.diagram.TypeValue').FOREIGN

        # replace picture shape

        shape.getForeignData().setValue(file_content)

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "ReplacePictureShape.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Replaced picture shape successfully!"

{{< /highlight >}}
## **下载运行代码**
下载**替换Visio Diagram (Aspose.Diagram)的图片形状**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/replacepictureshape.rb)
