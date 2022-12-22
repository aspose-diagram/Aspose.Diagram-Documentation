---
title: 在 Ruby 中添加对动态网格和连接点的支持
type: docs
weight: 10
url: /zh/java/add-support-of-dynamic-grids-and-connection-points-in-ruby/
---
## **Aspose.Diagram - 添加对动态网格和连接点的支持**
要添加对动态网格和连接点的支持，请使用**Aspose.Diagram Java 红宝石** 只需调用**添加动态网格和连接点**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# get window object by index

window = diagram.getWindows().get(0)

\# check dynamic grid option

window.setDynamicGridEnabled(1)

\# check connection points option

window.setShowConnectionPoints(1)

\# Save as VDX

diagram.save(data_dir + "AddDynamicGridsAndConnectionPoints.vsx", Rjb::import('com.aspose.diagram.SaveFileFormat').VSX)

puts "Added Support of Dynamic Grids and Connection Points in the Visio Drawings."

{{< /highlight >}}
## **下载运行代码**
下载**添加对动态网格和连接点的支持 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/adddynamicgridsandconnectionpoints.rb)
