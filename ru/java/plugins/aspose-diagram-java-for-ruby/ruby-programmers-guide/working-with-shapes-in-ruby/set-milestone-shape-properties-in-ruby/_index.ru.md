---
title: Установите свойства формы вехи в Ruby
type: docs
weight: 110
url: /ru/java/set-milestone-shape-properties-in-ruby/
---
## **Aspose.Diagram - Установить свойства формы вехи**
 Чтобы задать свойства формы вехи, используя**Aspose.Diagram Java для рубина** , просто вызовите**SetMilestoneShapeProperties** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

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
## **Скачать рабочий код**
 Скачать**Задать свойства формы вехи (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setmilestoneshapeproperties.rb)
