---
title: 在 Ruby 中设置连接器类型形状的外观 Visio
type: docs
weight: 100
url: /zh/java/set-appearance-of-the-connector-type-shape-in-visio-in-ruby/
---
## **Aspose.Diagram - 在 Visio 中设置连接器类型形状的外观**
要在 Visio 中设置连接器类型形状的外观，请使用**Aspose.Diagram Java 红宝石** 只需调用**设置形状外观**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Access a particular page

page = diagram.getPages().getPage("Flow 1")

\# get a particular connector shape

shape = page.getShapes().getShape(1)

\# set dynamic connector appearance

shape.setConnectorsType(Rjb::import('com.aspose.diagram.ConnectorsTypeValue').STRAIGHT_LINES)

\# Save diagram

diagram.save(data_dir + "SetShapeAppearance.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set appearnce of the connector type shape."

{{< /highlight >}}
## **下载运行代码**
下载**Visio（Aspose.Diagram）中设置连接器类型形状的外观**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapeappearance.rb)
