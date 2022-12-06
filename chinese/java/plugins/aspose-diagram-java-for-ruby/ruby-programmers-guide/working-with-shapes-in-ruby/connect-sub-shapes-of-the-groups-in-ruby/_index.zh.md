---
title: 在 Ruby 中连接组的子形状
type: docs
weight: 20
url: /zh/java/connect-sub-shapes-of-the-groups-in-ruby/
---
## **Aspose.Diagram - 连接组的子形状**
使用以下方法连接组的子形状**Aspose.Diagram Java 红宝石** 只需调用**连接子形状**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Access a particular page

page = diagram.getPages().getPage("Flow 1")

\# Set sub shape ids

shape_from_id = 1

shape_to_id = 9

\# Initialize connector shape

shape = Rjb::import('com.aspose.diagram.Shape').new

shape.getLine().getEndArrow().setValue(5)

shape.getLine().getLineWeight().setValue(0.01388)

\# Add shape

connecter_id = diagram.addShape(shape, "Dynamic connector", page.getID())

\# Connect sub-shapes

connection_point_place = Rjb::import('com.aspose.diagram.ConnectionPointPlace')

page.connectShapesViaConnector(shape_from_id, connection_point_place.RIGHT, shape_to_id, connection_point_place.LEFT, connecter_id)

\# Save diagram

diagram.save(data_dir + "ConnectSubShapes.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Connected sub-shapes of a group."

{{< /highlight >}}
## **下载运行代码**
下载**连接组的子形状 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/connectsubshapes.rb)
