---
title: Ruby'de Kilometre Taşı Şekli Özelliklerini Ayarlama
type: docs
weight: 110
url: /tr/java/set-milestone-shape-properties-in-ruby/
---
## **Aspose.Diagram - Kilometre Taşı Şekli Özelliklerini Ayarla**
 Kilometre Taşı Şekli Özelliklerini Ayarlamak için**Yakut için Aspose.Diagram Java** , sadece çağırmak**SetMilestoneShapeProperties** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

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
## **Çalışan Kodu İndir**
 İndirmek**Kilometre Taşı Şekli Özelliklerini Ayarla (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setmilestoneshapeproperties.rb)
