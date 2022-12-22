---
title: 在 Ruby 中以合适的角度旋转形状
type: docs
weight: 80
url: /zh/java/rotate-a-shape-with-suitable-angle-in-ruby/
---
## **Aspose.Diagram - 以合适的角度旋转形状**
使用合适的角度旋转形状**Aspose.Diagram Java 红宝石** 只需调用**旋转形状**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Add a shape and set the angle

diagram.getPages().getPage(0).getShapes().getShape(1).setAngle(190)

\# Save diagram

diagram.save(data_dir + "RotateShape.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Rotated shape."

{{< /highlight >}}
## **下载运行代码**
下载**以合适的角度旋转形状 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/rotateshape.rb)
