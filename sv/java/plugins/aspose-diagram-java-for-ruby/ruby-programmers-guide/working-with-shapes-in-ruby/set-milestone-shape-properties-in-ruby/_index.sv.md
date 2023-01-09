---
title: Ställ in Milestone Shape Properties i Ruby
type: docs
weight: 110
url: /sv/java/set-milestone-shape-properties-in-ruby/
---
## **Aspose.Diagram - Ställ in egenskaper för milstolpeform**
 För att ställa in Milstolpeformegenskaper med hjälp av**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**SetMilestoneShapeProperties** modul. Här kan du se exempelkod.

**Ruby kod**

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
## **Ladda ner Running Code**
 Ladda ner**Ställ in egenskaper för milstolpeform (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setmilestoneshapeproperties.rb)
