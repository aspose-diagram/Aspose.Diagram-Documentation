---
title: قم بتعيين خصائص شكل Milestone في Ruby
type: docs
weight: 110
url: /ar/java/set-milestone-shape-properties-in-ruby/
---
## **Aspose.Diagram - تعيين خصائص الشكل الرئيسي**
 لتعيين خصائص الشكل الرئيسي باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**SetMilestoneShapeProperties** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

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
## **قم بتنزيل كود التشغيل**
 تحميل**تعيين خصائص الشكل الرئيسي (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setmilestoneshapeproperties.rb)
