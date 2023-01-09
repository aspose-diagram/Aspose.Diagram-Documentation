---
title: 在 Ruby 中设置里程碑形状属性
type: docs
weight: 110
url: /zh/java/set-milestone-shape-properties-in-ruby/
---
## **Aspose.Diagram - 设置里程碑形状属性**
设置里程碑形状属性使用**Aspose.Diagram Java 红宝石** 只需调用**设置里程碑形状属性**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

shape_id = 1

\# Get timeline shape

milestone = diagram.getPages().getPage("Flow 1").getShapes().getShape(shape_id)

\# Initialize MilestoneHelper object

milestone_helper = Rjb::import('com.aspose.diagram.MilestoneHelper').new(milestone)

\# Set date format

milestone_helper.setDateFormat(21)

\# Set auto update flag

milestone_helper.setAutoUpdate(true)

\# Set milestone type

milestone_helper.setType(6)

\# Save diagram

diagram.save(data_dir + "SetMilestoneShapeProperties.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set milestone shape properties."

{{< /highlight >}}
## **下载运行代码**
下载**设置里程碑形状属性 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setmilestoneshapeproperties.rb)
